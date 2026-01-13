# Quick Start Guide

**Goal:** Get you coding and building TODAY. No overthinking, no delays.

## What You'll Do in the Next 4 Hours

This guide follows [Day 1 of the 90-day plan](./AI-ENGINEER-TRANSITION-PLAN.md#day-1-foundation-setup).

---

## Hour 1: Environment Setup (Complete this FIRST)

### Step 1: Install Core Tools (30 minutes)

**On your MacBook M4:**

1. **Install Homebrew** (package manager for Mac)
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. **Install Python via pyenv** (better than system Python)
```bash
brew install pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
source ~/.zshrc
pyenv install 3.11.7
pyenv global 3.11.7
```

3. **Install Poetry** (Python package manager)
```bash
curl -sSL https://install.python-poetry.org | python3 -
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

4. **Install Docker Desktop**
- Download: https://www.docker.com/products/docker-desktop/
- Install and start Docker Desktop
- Verify: `docker --version` (should show version 24+)

5. **Install VS Code**
- Download: https://code.visualstudio.com/
- Install these extensions (search in Extensions panel):
  - Python (by Microsoft)
  - Docker (by Microsoft)
  - Pylance (by Microsoft)

### Step 2: Set Up GitHub Repository (15 minutes)

```bash
# Create your main projects directory
mkdir -p ~/furywren-ai-lab
cd ~/furywren-ai-lab

# Initialize git
git init
git branch -M main

# Create repository structure
mkdir -p {agents,workflows,datasets,docs,scripts}

# Create initial README
cat > README.md << 'EOF'
# FuryWren AI Lab - Personal Projects

Building AI-powered security tools and automation workflows.

## Projects

1. IOC Enrichment Script (Week 1)
2. More coming soon...

EOF

# First commit
git add .
git commit -m "Initial commit: Project structure"

# Create GitHub repo (you'll do this manually):
# 1. Go to github.com and create new repository: "furywren-ai-lab"
# 2. Don't initialize with README (we already have one)
# 3. Then run:
# git remote add origin https://github.com/YOUR_USERNAME/furywren-ai-lab.git
# git push -u origin main
```

### Step 3: Update LinkedIn (15 minutes)

**Update your headline:**
```
Senior Threat Intelligence Analyst | Transitioning to AI-Powered Security Engineering | Building Autonomous Detection Systems
```

**Update your About section to include:**
```
Currently building AI-powered threat intelligence and security automation systems in my home lab. Bridging 15 years of intelligence tradecraft with modern AI engineering to solve complex security challenges.

🔨 Current Projects:
- AI agents for automated threat analysis
- OSINT collection and correlation pipelines
- Detection engineering with ML/AI

🎯 Seeking remote roles in: AI Security Engineering, Threat Intelligence Engineering, Detection Engineering

📂 Portfolio: github.com/YOUR_USERNAME/furywren-ai-lab
```

---

## Hour 2: First Python Script (Your First Win)

### Project: IOC Parser

**What it does:** Takes a text file with mixed content (IPs, domains, hashes) and extracts only the IOCs, categorizes them, and exports to JSON.

### Step 1: Create Project (5 minutes)

```bash
cd ~/furywren-ai-lab
mkdir -p agents/ioc-parser
cd agents/ioc-parser

# Initialize poetry project
poetry init --no-interaction --name ioc-parser --python "^3.11"
poetry add ipaddress
```

### Step 2: Create Sample Data (5 minutes)

```bash
cat > sample_intel.txt << 'EOF'
Threat Report: APT29 Activity

The following indicators were observed:

IP addresses seen:
192.168.1.100 (internal, ignore)
45.142.212.61
103.75.201.2
8.8.8.8 (Google DNS)

Domains:
malicious-site.com
secure-login.org
google.com (benign)

File hashes (SHA256):
3c0b4a7c4c7c3e3d3e3f3e3d3e3f3e3d3e3f3e3d3e3f3e3d3e3f3e3d3e3f3e3d
a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6q7r8s9t0u1v2w3x4y5z6a7b8c9d0e1f2

Contact: analyst@example.com for questions.
EOF
```

### Step 3: Write the Script (30 minutes)

```bash
# Create main script
cat > ioc_parser.py << 'EOF'
#!/usr/bin/env python3
"""
IOC Parser - Extract and categorize indicators of compromise
"""

import re
import json
import ipaddress
from pathlib import Path
from typing import Dict, List

class IOCParser:
    def __init__(self):
        # Regex patterns for different IOC types
        self.patterns = {
            'ip': r'\b(?:[0-9]{1,3}\.){3}[0-9]{1,3}\b',
            'domain': r'\b(?:[a-zA-Z0-9-]+\.)+[a-zA-Z]{2,}\b',
            'sha256': r'\b[a-fA-F0-9]{64}\b',
            'md5': r'\b[a-fA-F0-9]{32}\b',
            'email': r'\b[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}\b'
        }

        # Known benign indicators to filter out
        self.whitelist = {
            'ip': ['8.8.8.8', '1.1.1.1'],  # Common DNS servers
            'domain': ['google.com', 'microsoft.com', 'apple.com', 'example.com']
        }

    def is_private_ip(self, ip: str) -> bool:
        """Check if IP is private/internal"""
        try:
            return ipaddress.ip_address(ip).is_private
        except ValueError:
            return False

    def extract_iocs(self, text: str) -> Dict[str, List[str]]:
        """Extract all IOCs from text"""
        iocs = {
            'ip_addresses': [],
            'domains': [],
            'file_hashes': [],
            'emails': []
        }

        # Extract IPs (filter private and whitelisted)
        ips = re.findall(self.patterns['ip'], text)
        for ip in set(ips):
            if not self.is_private_ip(ip) and ip not in self.whitelist['ip']:
                iocs['ip_addresses'].append(ip)

        # Extract domains (filter whitelisted)
        domains = re.findall(self.patterns['domain'], text)
        for domain in set(domains):
            # Exclude emails from domains
            if '@' not in domain and domain.lower() not in self.whitelist['domain']:
                iocs['domains'].append(domain)

        # Extract file hashes
        sha256_hashes = re.findall(self.patterns['sha256'], text)
        md5_hashes = re.findall(self.patterns['md5'], text)
        iocs['file_hashes'] = list(set(sha256_hashes + md5_hashes))

        # Extract emails (optional, for context)
        emails = re.findall(self.patterns['email'], text)
        iocs['emails'] = list(set(emails))

        return iocs

    def parse_file(self, filepath: str) -> Dict:
        """Parse IOCs from a file"""
        with open(filepath, 'r', encoding='utf-8') as f:
            text = f.read()

        iocs = self.extract_iocs(text)

        # Add metadata
        result = {
            'source_file': filepath,
            'total_indicators': sum(len(v) for k, v in iocs.items() if k != 'emails'),
            'indicators': iocs
        }

        return result

    def save_json(self, data: Dict, output_file: str):
        """Save results to JSON file"""
        with open(output_file, 'w', encoding='utf-8') as f:
            json.dump(data, f, indent=2)
        print(f"✓ Results saved to {output_file}")


def main():
    # Create parser instance
    parser = IOCParser()

    # Parse the sample file
    print("Parsing IOCs from sample_intel.txt...")
    results = parser.parse_file('sample_intel.txt')

    # Display results
    print("\n" + "="*50)
    print("IOC EXTRACTION RESULTS")
    print("="*50)
    print(f"\nTotal Indicators Found: {results['total_indicators']}\n")

    for category, items in results['indicators'].items():
        if category != 'emails' and items:
            print(f"{category.upper()}:")
            for item in items:
                print(f"  • {item}")
            print()

    # Save to JSON
    parser.save_json(results, 'iocs.json')
    print("\n✓ Analysis complete!")


if __name__ == '__main__':
    main()
EOF

chmod +x ioc_parser.py
```

### Step 4: Run It (5 minutes)

```bash
# Run the script
poetry run python ioc_parser.py

# Check the output
cat iocs.json
```

### Step 5: Push to GitHub (5 minutes)

```bash
# Create README for this project
cat > README.md << 'EOF'
# IOC Parser

Extracts and categorizes Indicators of Compromise (IOCs) from threat intelligence reports.

## Features
- Extracts IPs, domains, and file hashes
- Filters private IPs and known benign domains
- Exports to JSON format
- Easy to integrate into automation workflows

## Usage
```bash
poetry install
poetry run python ioc_parser.py
```

## Example Output
```json
{
  "indicators": {
    "ip_addresses": ["45.142.212.61", "103.75.201.2"],
    "domains": ["malicious-site.com", "secure-login.org"],
    "file_hashes": ["3c0b4a7c..."]
  }
}
```

## Next Steps
- Add API enrichment (VirusTotal, AbuseIPDB)
- Support multiple file formats (PDF, CSV)
- Build web interface
EOF

# Commit and push
cd ~/furywren-ai-lab
git add .
git commit -m "Add IOC Parser - first Python security tool"
git push origin main
```

**🎉 CONGRATULATIONS! You just built and deployed your first security tool!**

---

## Hour 3: First Docker Container

### What You'll Build
Containerize the IOC parser so it can run anywhere (your NAS, cloud, etc.)

### Step 1: Create Dockerfile (10 minutes)

```bash
cd ~/furywren-ai-lab/agents/ioc-parser

cat > Dockerfile << 'EOF'
FROM python:3.11-slim

WORKDIR /app

# Install poetry
RUN pip install poetry

# Copy project files
COPY pyproject.toml poetry.lock* ./
COPY ioc_parser.py ./
COPY sample_intel.txt ./

# Install dependencies
RUN poetry config virtualenvs.create false \
    && poetry install --no-interaction --no-ansi

# Run the script
CMD ["python", "ioc_parser.py"]
EOF
```

### Step 2: Create .dockerignore (2 minutes)

```bash
cat > .dockerignore << 'EOF'
__pycache__
*.pyc
.git
.venv
*.json
EOF
```

### Step 3: Build and Run (10 minutes)

```bash
# Build the Docker image
docker build -t ioc-parser:v1 .

# Run the container
docker run --rm ioc-parser:v1

# Run with volume to get output files
docker run --rm -v $(pwd):/app/output ioc-parser:v1

# Check the image exists
docker images | grep ioc-parser
```

### Step 4: Update README and Push (8 minutes)

```bash
# Add Docker section to README
cat >> README.md << 'EOF'

## Docker Usage

Build:
```bash
docker build -t ioc-parser:v1 .
```

Run:
```bash
docker run --rm -v $(pwd):/app/output ioc-parser:v1
```
EOF

# Commit
git add .
git commit -m "Add Docker support to IOC Parser"
git push origin main
```

**🎉 You now have a containerized security tool!**

---

## Hour 4: Job Applications & LinkedIn Post

### Step 1: Update Resume (20 minutes)

**Add this section to your resume under "CYBERSECURITY AND AI PROJECTS":**

```
FuryWren AI Lab (2025 - Present)
Building production-grade AI-powered security tools and automation workflows

• Developed IOC extraction tool with Python for automated threat intelligence parsing
  (regex patterns, IP validation, JSON export) - deployed as Docker container
• Designed home lab infrastructure with enterprise security stack: Wazuh SIEM/XDR,
  Suricata IDS, MISP threat intelligence platform, and PostgreSQL for data analytics
• Implementing AI agents using LangChain for automated alert triage and
  threat correlation across multiple intelligence sources

Portfolio: github.com/YOUR_USERNAME/furywren-ai-lab
```

### Step 2: Apply to 3 Jobs (30 minutes)

**Target companies (check their careers pages):**

1. **Google Mandiant** - Search for "Threat Intelligence" or "Detection Engineer"
2. **CrowdStrike** - Search for "Threat Analyst" or "Security Engineer"
3. **Recorded Future** - Search for "Threat Intelligence Analyst"

**Cover letter template:**

```
Dear Hiring Manager,

I am a Senior Threat Intelligence Analyst with 15 years of experience in high-stakes threat investigations for a U.S. Intelligence Agency, now transitioning to AI-powered security engineering roles. I am particularly drawn to [COMPANY]'s approach to [mention something specific about their tech/mission].

What makes me different: I combine deep intelligence tradecraft with hands-on AI engineering. I'm not just learning about AI security—I'm building it. My current projects include:

• AI agents for automated threat intelligence correlation and alert triage
• Production security infrastructure (Wazuh SIEM, Suricata IDS) deployed in containers
• Python tools for IOC extraction and enrichment (see: github.com/YOUR_USERNAME/furywren-ai-lab)

I understand threat actor methodologies from years of disruption operations, and I'm now applying that knowledge to build autonomous detection systems. This is the hybrid skillset that roles like [JOB TITLE] require.

I am seeking 100% remote positions with up to 25% travel. I would welcome the opportunity to discuss how my intelligence background and emerging AI capabilities can contribute to [COMPANY]'s mission.

Best regards,
Jay Gulyash
jaygulyash@gmail.com
(970) 875-8268
GitHub: github.com/YOUR_USERNAME/furywren-ai-lab
```

### Step 3: LinkedIn Post (10 minutes)

**Post this on LinkedIn:**

```
Day 1 of my transition from traditional threat intelligence to AI-powered security engineering. 🚀

What I built today:
✅ IOC Parser in Python - extracts indicators from threat reports
✅ Dockerized it for portability
✅ Pushed to GitHub as open-source tool

Why this matters: Threat intel teams spend hours manually extracting IOCs from reports. This automates it. Next up: Adding AI-powered enrichment with LLMs.

I'm combining 15 years of intelligence tradecraft with modern AI engineering. If you're working on AI security tools, autonomous detection systems, or threat intelligence automation, let's connect. 🔐

Check out the code: github.com/YOUR_USERNAME/furywren-ai-lab

#ThreatIntelligence #AIEngineering #CyberSecurity #Python #Docker
```

---

## What You Accomplished Today

1. ✅ Set up professional development environment
2. ✅ Built your first Python security tool (IOC Parser)
3. ✅ Learned Docker basics and containerized your tool
4. ✅ Created GitHub portfolio with working code
5. ✅ Updated resume with practical projects
6. ✅ Applied to 3 target companies
7. ✅ Established LinkedIn presence as AI security engineer

**Most importantly: YOU SHIPPED CODE.** Not plans, not notes—working software.

---

## Tomorrow (Day 2): Docker Deep Dive

Follow the [Day 2 guide in the main plan](./AI-ENGINEER-TRANSITION-PLAN.md#day-2-docker-deep-dive):
- Deploy Wazuh SIEM in Docker
- Deploy Suricata IDS to monitor your network
- Start building your security detection stack

---

## Troubleshooting

**Python issues:**
```bash
# If pyenv doesn't work:
brew reinstall pyenv
# Then restart terminal

# If poetry not found:
curl -sSL https://install.python-poetry.org | python3 -
source ~/.zshrc
```

**Docker issues:**
```bash
# If Docker daemon not running:
# Open Docker Desktop app manually

# If permission issues:
sudo chmod 666 /var/run/docker.sock
```

**Git issues:**
```bash
# Configure git if first time:
git config --global user.name "Your Name"
git config --global user.email "jaygulyash@gmail.com"
```

---

## Key Principle

**Done is better than perfect.** Your IOC parser doesn't have to be the best IOC parser ever written. It just needs to work and demonstrate that you can:
1. Write Python code
2. Solve security problems
3. Use Docker
4. Ship working software

Everything else is iteration.

---

## Next Steps

After completing this quick start:

1. **Read the [full 90-day plan](./AI-ENGINEER-TRANSITION-PLAN.md)** to understand the big picture
2. **Follow Day 2 tomorrow** - don't skip ahead, build momentum
3. **Post daily updates on LinkedIn** - visibility matters for job search
4. **Keep applying to 2-3 jobs per day** - pipeline over perfection

**You're not just learning anymore. You're building. Keep the momentum going.**
