# AI Engineer Transition Plan
## 65% AI Native Engineer + 35% Cyber Threat Intel | Remote-Only

**Target Salary:** $165,000+
**Work Model:** 100% Remote with up to 25% travel
**Timeline:** Aggressive 90-day intensive with 180-day production-ready goal

---

## Executive Summary

You have a unique advantage: 15+ years of intelligence tradecraft, threat analysis, and operational experience. The market desperately needs professionals who can build AI-powered threat detection systems and understand both the technical and analytical sides. This plan focuses on **building, not just learning**—transforming your home lab into a production-grade portfolio that demonstrates enterprise-level capabilities.

**Critical Insight:** Your website can wait. Recruiters at Google Mandiant, CrowdStrike, and OpenAI care about your GitHub portfolio, working demos, and technical depth—not a polished marketing site. Focus 100% on building working systems for the next 90 days.

---

## Part 1: Top 10 Target Roles

Based on your background, here are the roles that align best with your transition:

### Tier 1: Primary Targets (Best Fit)
1. **AI-Powered Threat Intelligence Engineer** (CrowdStrike, Recorded Future, Google Mandiant)
   - Builds AI agents for threat hunting, IOC enrichment, and attribution
   - Combines your intel background with AI engineering
   - Salary: $165k-$220k

2. **Security AI/ML Engineer** (Anthropic, OpenAI, Cloudflare)
   - Develops AI safety systems and threat detection models
   - Focuses on LLM security, adversarial testing, and red teaming
   - Salary: $180k-$250k

3. **Cyber Threat Intelligence Analyst (AI-Focused)** (Google Mandiant, Microsoft, CrowdStrike)
   - Uses AI to automate CTI workflows, correlation, and reporting
   - Your strongest immediate fit with upskilling in AI automation
   - Salary: $150k-$200k

4. **Detection Engineering Lead** (Cloudflare, Datadog, Elastic)
   - Builds detection pipelines using ML/AI for anomaly detection
   - Develops SIEM content and threat hunting tools
   - Salary: $160k-$210k

5. **Security Automation Engineer** (Palo Alto Networks, Splunk, Wiz)
   - Creates automated incident response workflows
   - Integrates AI into SOC operations
   - Salary: $155k-$200k

### Tier 2: Growth Targets (6-12 Months Out)
6. **AI Solutions Architect (Security)** (AWS, Google Cloud, Microsoft Azure)
   - Designs AI-powered security solutions for enterprises
   - Requires deeper cloud architecture knowledge
   - Salary: $175k-$240k

7. **Security Research Engineer** (Trail of Bits, Bishop Fox, NCC Group)
   - Develops novel detection techniques and offensive AI tools
   - Combines research with practical engineering
   - Salary: $170k-$230k

8. **Threat Intelligence Platform Engineer** (Recorded Future, ThreatConnect, Anomali)
   - Builds CTI platforms and automation workflows
   - Backend development focus with AI integration
   - Salary: $160k-$210k

### Tier 3: Stretch Goals (12+ Months)
9. **AI Agent Engineer (Security Domain)** (10a Labs, stealth startups, VCs)
   - Builds autonomous agents for security operations
   - Cutting-edge LangChain, LangGraph, CrewAI work
   - Salary: $180k-$280k + equity

10. **Principal Security Engineer (AI/ML)** (Anthropic, OpenAI, Scale AI)
    - Senior IC role designing AI security infrastructure
    - Requires proven track record of production systems
    - Salary: $200k-$350k

---

## Part 2: Skills Gap Analysis

### What You Have (Strengths)
- Deep threat intelligence tradecraft and analytical expertise
- Understanding of adversary TTPs, threat actor attribution
- Experience with intelligence requirements and collection
- Proven ability to brief executives and produce intelligence products
- Clearance (TS/SCI) for national security roles if needed

### What You Need (90-Day Priorities)
1. **Python proficiency** (from beginner to intermediate)
2. **Docker and containerization** (working knowledge)
3. **AI agent frameworks** (LangChain, LangGraph, CrewAI)
4. **Vector databases** (Chroma, Pinecone, Qdrant)
5. **API development** (FastAPI, Flask)
6. **CI/CD pipelines** (GitHub Actions)
7. **Production deployments** (not just prototypes)

### What You Need (180-Day Goals)
8. Knowledge graphs (Neo4j, graph databases)
9. Advanced prompt engineering and LLM optimization
10. Kubernetes basics (optional but valuable)
11. Cloud platforms (AWS/GCP for hosting agents)

---

## Part 3: Immediate Action Plan (Days 1-7)

### Day 1: Foundation Setup
**Morning (2 hours)**
- [ ] Create dedicated GitHub repository: `furywren-ai-lab`
- [ ] Set up project structure: `/agents`, `/workflows`, `/datasets`, `/docs`
- [ ] Install VS Code with Python, Docker, and GitHub Copilot extensions
- [ ] Configure Git for commit signing (security best practice)

**Afternoon (3 hours)**
- [ ] Set up Python environment using `pyenv` and `poetry` (not Anaconda)
- [ ] Create first Docker container: Simple Python app with FastAPI
- [ ] Deploy "Hello World" API endpoint
- [ ] Document in README with architecture diagram

**Evening (1 hour)**
- [ ] Apply to 3 jobs (Google Mandiant, CrowdStrike, Recorded Future)
- [ ] Update LinkedIn headline: "Threat Intelligence Engineer | Building AI-Powered Security Systems"

**Tools Needed:** VS Code, Docker Desktop, GitHub account
**Cost:** $0

---

### Day 2: Docker Deep Dive
**Morning (3 hours)**
- [ ] Complete Docker tutorial: Build Wazuh container from scratch
- [ ] Learn Docker Compose: Multi-container setup (Wazuh + Elasticsearch + Kibana)
- [ ] Practice: Stop, start, rebuild, inspect logs

**Afternoon (3 hours)**
- [ ] Deploy Suricata IDS in Docker container
- [ ] Configure it to monitor your MacBook network traffic
- [ ] Generate alerts by visiting test sites (testmyids.com)
- [ ] Export logs to JSON, analyze with Python

**Evening (1 hour)**
- [ ] Write blog post (LinkedIn article): "Why I'm Containerizing My Security Lab"
- [ ] Share lessons learned, architecture diagram

**Tools Needed:** Docker Desktop, Suricata
**Cost:** $0

---

### Day 3: Python Fundamentals (Intelligence Focus)
**Morning (3 hours)**
- [ ] Python crash course: Variables, loops, functions, dictionaries
- [ ] Build script: Parse IOC list (IPs, domains, hashes) from text file
- [ ] Output: JSON file with categorized IOCs

**Afternoon (3 hours)**
- [ ] Learn `requests` library: Call VirusTotal API
- [ ] Script: Enrich IOCs with VT data (malicious score, country, ASN)
- [ ] Handle rate limits and errors gracefully

**Evening (1 hour)**
- [ ] Push script to GitHub with clear README
- [ ] Apply to 2 more jobs

**Tools Needed:** Python, VirusTotal API (free tier)
**Cost:** $0

---

### Day 4: First AI Agent
**Morning (4 hours)**
- [ ] Install LangChain and OpenAI SDK (or use Claude API)
- [ ] Build simple agent: "IOC Enrichment Assistant"
- [ ] Input: IP address or domain
- [ ] Output: Summary of threat intel from multiple sources

**Afternoon (2 hours)**
- [ ] Add web search capability using DuckDuckGo API (free)
- [ ] Test with known malicious IPs and benign domains
- [ ] Refine prompts for accuracy

**Evening (1 hour)**
- [ ] Create demo video: Screen recording showing agent in action
- [ ] Post to LinkedIn with code snippet

**Tools Needed:** LangChain, OpenAI API ($10 credit)
**Cost:** $10

---

### Day 5: Vector Database Introduction
**Morning (3 hours)**
- [ ] Learn vector embeddings: What they are, why they matter
- [ ] Set up Chroma DB locally (free, open-source)
- [ ] Load sample threat intel reports (CISA alerts, Mandiant reports)
- [ ] Create embeddings using OpenAI or local model

**Afternoon (3 hours)**
- [ ] Build semantic search: Query "ransomware targeting healthcare"
- [ ] Return relevant reports with similarity scores
- [ ] Compare to keyword search (show vector search is better)

**Evening (1 hour)**
- [ ] Document findings in GitHub repository
- [ ] Share on LinkedIn: "Why Vector Databases Matter for Threat Intelligence"

**Tools Needed:** Chroma, sentence-transformers
**Cost:** $5 (API calls)

---

### Day 6: n8n Automation Basics
**Morning (2 hours)**
- [ ] Deploy n8n locally using Docker (don't use Hostinger VPS yet)
- [ ] Create first workflow: Daily RSS feed aggregator
- [ ] Sources: Krebs on Security, Threatpost, The Hacker News
- [ ] Output: Send email digest or save to JSON

**Afternoon (3 hours)**
- [ ] Build workflow: Auto-enrich IOCs from RSS feeds
- [ ] Steps: Extract IOCs → Call VT API → Store in database
- [ ] Use n8n's built-in nodes (no Python yet)

**Evening (2 hours)**
- [ ] Set up Notion database for threat intel tracking
- [ ] Connect n8n to Notion API (free tier)
- [ ] Auto-populate database with daily threat intel

**Tools Needed:** n8n (Docker), Notion (free)
**Cost:** $0

---

### Day 7: Home Lab Architecture Planning
**Morning (2 hours)**
- [ ] Draw network diagram of your lab:
  - MacBook M4 (host) → Protectli VP2430 (firewall) → Synology NAS
  - Docker containers on NAS and MacBook
  - Twingate for secure remote access
- [ ] Identify what you'll run where (see Part 5)

**Afternoon (2 hours)**
- [ ] Set up proper network segmentation:
  - Home network: 192.168.1.0/24 (ISP router)
  - Lab network: 10.0.10.0/24 (Protectli OPNsense)
  - DMZ for exposed services: 10.0.20.0/24
- [ ] Configure Suricata on Raspberry Pi to monitor lab network

**Evening (3 hours)**
- [ ] Create GitHub project board for home lab build
- [ ] Tasks: "Set up Wazuh", "Deploy MISP", "Configure TwinGate", etc.
- [ ] Prioritize based on portfolio value (detection > infrastructure)

**Tools Needed:** Draw.io (free), OPNsense
**Cost:** $0

---

## Week 1 Summary
By the end of Day 7, you will have:
- Working Python scripts for IOC enrichment
- First AI agent deployed locally
- Docker containers running security tools
- n8n workflows automating threat intel collection
- Clear home lab architecture plan
- 5 job applications submitted
- Active LinkedIn presence with technical content

**Total Cost Week 1:** $15
**Portfolio Items:** 3 (GitHub repos, demo video, technical articles)

---

## Part 4: 90-Day Roadmap

### Weeks 1-4: Foundation (CURRENT FOCUS)
**Goal:** Build core Python, Docker, and AI agent skills

**Week 1:** Docker, Python basics, first agent (see Days 1-7 above)

**Week 2: Advanced Python for Security**
- [ ] Learn pandas for data analysis (threat intel datasets)
- [ ] Build script: Analyze PCAP files and extract IOCs
- [ ] Create visualization: Top talkers, protocol distribution
- [ ] Deploy as Jupyter notebook in Docker container
- [ ] **Project:** "PCAP Analysis Toolkit" → GitHub

**Week 3: API Development**
- [ ] Learn FastAPI framework
- [ ] Build REST API for IOC enrichment agent (from Day 4)
- [ ] Endpoints: `/enrich`, `/search`, `/report`
- [ ] Add authentication (API keys)
- [ ] Deploy with Docker Compose
- [ ] **Project:** "Threat Intel API" → GitHub + demo video

**Week 4: Production Agent #1**
- [ ] Build "Alert Triage Agent"
  - Input: SIEM alert (JSON)
  - Process: Enrich IOCs, check context, assess severity
  - Output: Prioritized recommendation with evidence
- [ ] Use LangChain with Claude API
- [ ] Add vector database for historical context
- [ ] Deploy to Docker container with FastAPI frontend
- [ ] **Project:** "AI Alert Triage System" → GitHub + YouTube demo
- [ ] Apply this to 10 more jobs with portfolio link in resume

**Milestone 1:** 3 production-ready projects on GitHub
**Cost Weeks 1-4:** $75 (API calls, domains optional)

---

### Weeks 5-8: Intelligence Automation Hub
**Goal:** Build enterprise-grade automation workflows with n8n

**Week 5: OSINT Collection Pipeline**
- [ ] n8n workflows for:
  - RSS feed aggregation (30+ security sources)
  - Twitter/X monitoring (security researchers)
  - GitHub security advisories
  - CISA alerts
- [ ] Store in PostgreSQL database (Docker container)
- [ ] Build search interface with Streamlit (Python UI framework)
- [ ] **Project:** "OSINT Aggregation Platform"

**Week 6: Automated IOC Enrichment**
- [ ] n8n workflow triggered by new IOCs
- [ ] Multi-source enrichment: VT, AbuseIPDB, Shodan, URLScan
- [ ] Store results in vector database (Qdrant)
- [ ] Generate PDF report with executive summary
- [ ] **Project:** "Autonomous IOC Processor"

**Week 7: Geopolitical Intelligence Correlator**
- [ ] Integrate GDELT and ACLED datasets
- [ ] Use LLM to correlate geopolitical events with cyber activity
- [ ] Example: "Ukraine conflict → increase in Russian APT activity"
- [ ] Build daily briefing generator (automated email)
- [ ] **Project:** "Geo-Cyber Intelligence Hub"

**Week 8: Knowledge Graph (Neo4j)**
- [ ] Set up Neo4j in Docker
- [ ] Model: Threat actors → TTPs → IOCs → Victims
- [ ] Populate with threat intel from weeks 5-7
- [ ] Build graph query interface (Streamlit)
- [ ] Demonstrate relationship discovery: "Which APT groups target healthcare?"
- [ ] **Project:** "Threat Intelligence Knowledge Graph"

**Milestone 2:** Intelligence Automation Hub fully operational
**Cost Weeks 5-8:** $100 (APIs, hosting)

---

### Weeks 9-12: Advanced AI Agents
**Goal:** Build multi-agent systems for security operations

**Week 9: Multi-Agent CTI System**
- [ ] Learn LangGraph (agent orchestration)
- [ ] Build team of agents:
  - Collector Agent (gathers data)
  - Analyst Agent (interprets findings)
  - Reporter Agent (writes briefings)
  - QA Agent (validates outputs)
- [ ] Implement RAG (Retrieval-Augmented Generation) with vector DB
- [ ] **Project:** "Multi-Agent CTI Analyst"

**Week 10: Detection Engineering Agent**
- [ ] Agent that generates SIEM rules from threat descriptions
- [ ] Input: "Detect lateral movement using WMI"
- [ ] Output: Sigma rules, Wazuh rules, KQL queries
- [ ] Validate rules in test environment (Wazuh)
- [ ] **Project:** "AI Detection Engineer"

**Week 11: Incident Response Orchestrator**
- [ ] Build agent that automates IR workflows
- [ ] Steps: Alert triage → Containment recommendations → Remediation playbook
- [ ] Integrate with MISP for IOC sharing
- [ ] Demonstrate with test scenarios
- [ ] **Project:** "AI IR Orchestrator"

**Week 12: Portfolio Consolidation**
- [ ] Polish all GitHub repositories:
  - Clear READMEs with architecture diagrams
  - Demo videos for each project
  - Installation guides
- [ ] Create portfolio site (simple GitHub Pages, not furywrenlabs.io)
- [ ] Write case studies for top 3 projects
- [ ] Update resume with project links
- [ ] Apply to 20 more jobs with complete portfolio

**Milestone 3:** 8-10 production projects showcasing AI + security
**Cost Weeks 9-12:** $150 (increased API usage, cloud hosting)

---

## Part 5: Home Lab Setup Guide

### Network Architecture
```
[ISP Router] (192.168.1.0/24)
    ↓
[Protectli VP2430 - OPNsense] (Firewall/Gateway)
    ↓
    ├─ [Home Network] (192.168.1.0/24) → Personal devices
    ├─ [Lab Network] (10.0.10.0/24) → Lab infrastructure
    │   ├─ MacBook M4 (10.0.10.10)
    │   ├─ Synology NAS (10.0.10.20)
    │   ├─ MacBook M2 (10.0.10.30)
    │   └─ Raspberry Pi 5 (10.0.10.40) - Suricata monitoring
    └─ [DMZ] (10.0.20.0/24) → Public-facing services (future)
```

### Phase 1: Network Foundation (Week 1-2)
**Priority: Medium** (You can develop without perfect segmentation initially)

1. **Configure Protectli VP2430 OPNsense**
   - Set up VLAN for lab network (10.0.10.0/24)
   - Configure firewall rules: Lab → Internet (allow), Lab → Home (block)
   - Install Zenarmor plugin for IDS/IPS
   - Install WireGuard for VPN access
   - Time: 4 hours
   - Cost: $0 (already own hardware)

2. **Set up Network Monitoring (Raspberry Pi 5)**
   - Install Suricata with Emerging Threats ruleset
   - Configure to mirror lab network traffic (span port on NETGEAR switch)
   - Send logs to Wazuh on NAS
   - Time: 3 hours
   - Cost: $0

3. **Configure TwinGate**
   - Deploy connector on Synology NAS (Docker)
   - Add MacBooks as endpoints
   - Test remote access to lab network
   - Time: 2 hours
   - Cost: $0 (free tier)

---

### Phase 2: Core Services on Synology NAS (Week 2-3)
**Priority: HIGH** (Essential for your projects)

Deploy these containers on NAS using Docker Compose:

1. **Wazuh SIEM/XDR** (Detection engineering practice)
   - Wazuh Manager + Elasticsearch + Kibana
   - Connect MacBooks as agents
   - Create custom detection rules
   - Time: 6 hours
   - Cost: $0
   - Resources: 8GB RAM, 200GB storage

2. **MISP Threat Intel Platform**
   - Central repository for IOCs
   - Integrate with your n8n workflows (auto-populate from feeds)
   - Practice API usage (critical skill)
   - Time: 4 hours
   - Cost: $0
   - Resources: 4GB RAM, 50GB storage

3. **PostgreSQL Database**
   - Store threat intel, IOCs, analysis results
   - Used by multiple projects
   - Time: 2 hours
   - Cost: $0
   - Resources: 2GB RAM, 20GB storage

4. **Qdrant Vector Database**
   - Semantic search for threat intel documents
   - RAG for AI agents
   - Time: 3 hours
   - Cost: $0
   - Resources: 4GB RAM, 50GB storage

5. **n8n (Local Instance)**
   - Keep Hostinger VPS for production workflows
   - Run local n8n for development/testing
   - Time: 2 hours
   - Cost: $0
   - Resources: 2GB RAM, 10GB storage

**Total NAS Resources Used:** 20GB RAM (leaves 12GB free), 330GB storage (plenty available)

---

### Phase 3: Development Environment on MacBook M4 (Week 1, ongoing)
**Priority: CRITICAL** (Your primary workspace)

1. **VS Code Setup**
   - Extensions: Python, Docker, GitHub Copilot, Jupyter
   - Time: 1 hour
   - Cost: $10/month (GitHub Copilot - optional but valuable)

2. **Python Environment**
   - Install `pyenv` (Python version manager)
   - Install `poetry` (dependency management, better than pip)
   - Create virtual environments per project
   - Time: 2 hours
   - Cost: $0

3. **Docker Desktop**
   - Run dev containers on MacBook
   - Push production containers to NAS
   - Time: 1 hour
   - Cost: $0

4. **Testing Environment**
   - Kali Linux (Parallels or UTM): Offensive security testing
   - Metasploitable3 (Docker or VM): Vulnerable target
   - Time: 4 hours
   - Cost: $0 (use UTM, free alternative to Parallels)

---

### Phase 4: Cloud Infrastructure (Week 6-8)
**Priority: MEDIUM** (Important for job applications)

1. **AWS Free Tier Setup**
   - Deploy detection engineering projects
   - EC2 instances for hosting agents
   - S3 for dataset storage
   - Lambda for serverless functions
   - Time: 8 hours (spread across 3 weeks)
   - Cost: $20/month (beyond free tier)

2. **GitHub Actions CI/CD**
   - Automate testing and deployment
   - Build Docker images on commit
   - Deploy to AWS EC2 or NAS
   - Time: 6 hours
   - Cost: $0

---

### Home Lab Infrastructure Priority Order

**Immediate (Week 1-2):**
1. Docker on MacBook M4 ✓
2. Python environment ✓
3. TwinGate (remote access) ✓
4. Wazuh on NAS ✓

**Short-term (Week 3-4):**
5. PostgreSQL on NAS ✓
6. MISP on NAS ✓
7. n8n local instance ✓
8. Suricata on Raspberry Pi ✓

**Medium-term (Week 5-8):**
9. Qdrant vector database ✓
10. Neo4j knowledge graph ✓
11. Protectli OPNsense (proper segmentation) ✓

**Later (Week 9-12):**
12. AWS cloud integration ✓
13. Advanced network monitoring ✓

---

## Part 6: Production Projects (Design → Prototype → Production)

### Project 1: AI-Powered Alert Triage System
**Timeline:** Weeks 3-4
**Value:** Directly applicable to SOC roles

**Design Phase (Days 1-2)**
- Define requirements: SIEM alert → AI analysis → priority recommendation
- Architecture: FastAPI → LangChain Agent → Vector DB → Output JSON/PDF
- Threat model: What alerts? (Wazuh, Suricata, manual input)

**Prototype Phase (Days 3-7)**
- Build core agent with LangChain
- Test with 10 sample alerts (mix of true/false positives)
- Iterate on prompts until accuracy > 80%

**Production Phase (Days 8-14)**
- Add FastAPI REST interface
- Implement authentication (API keys)
- Create Docker container
- Deploy to NAS with monitoring
- Write documentation and demo video
- Add to GitHub portfolio

**Deliverables:**
- GitHub repo with code, README, architecture diagram
- 5-minute demo video showing real alerts
- Blog post: "How I Built an AI SOC Analyst"

---

### Project 2: Intelligence Automation Hub (n8n)
**Timeline:** Weeks 5-7
**Value:** Shows end-to-end automation skills

**Design Phase (Week 5, Days 1-2)**
- Map data sources: RSS, Twitter, GitHub, CISA, GDELT
- Design workflows: Collection → Enrichment → Storage → Analysis → Reporting
- Database schema: PostgreSQL for structured data, Qdrant for semantic search

**Prototype Phase (Week 5, Days 3-7)**
- Build basic n8n workflows (one per data source)
- Test data ingestion and storage
- Create simple search interface (CLI or Streamlit)

**Production Phase (Weeks 6-7)**
- Advanced workflows:
  - Auto-enrich IOCs with VT, AbuseIPDB, Shodan
  - Generate daily threat brief (LLM summarization)
  - Correlate geopolitical events with cyber activity
- Build web interface (Streamlit)
- Deploy entire stack with Docker Compose
- Set up monitoring and alerting

**Deliverables:**
- GitHub repo with n8n workflow exports, Docker Compose file
- Live demo (accessible via TwinGate or public URL)
- Case study: "90 Days of Automated Threat Intel"

---

### Project 3: Threat Intelligence Knowledge Graph
**Timeline:** Weeks 8-9
**Value:** Unique differentiator, shows advanced data engineering

**Design Phase (Week 8, Days 1-3)**
- Graph schema: Entities (Threat Actor, TTP, IOC, Campaign, Victim) and relationships
- Data sources: MISP, MITRE ATT&CK, your collected intel
- Queries: "Which APTs use spearphishing?" "What TTPs target healthcare?"

**Prototype Phase (Week 8, Days 4-7)**
- Set up Neo4j in Docker
- Populate with sample data (MITRE ATT&CK framework)
- Write Cypher queries to extract insights

**Production Phase (Week 9)**
- Automate data ingestion from MISP and n8n workflows
- Build query interface (Streamlit or custom web app)
- Add LLM agent that can query graph in natural language
  - User: "Show me ransomware targeting hospitals"
  - Agent: Translates to Cypher, executes, interprets results
- Deploy with monitoring

**Deliverables:**
- GitHub repo with graph schema, ingestion scripts
- Interactive demo with complex queries
- Technical write-up: "Building a Cyber Threat Knowledge Graph"

---

### Project 4: Multi-Agent CTI System
**Timeline:** Weeks 10-11
**Value:** Cutting-edge, aligns with AI Engineer roles

**Design Phase (Week 10, Days 1-2)**
- Agent roles:
  - Collector: Gathers raw data (OSINT, feeds)
  - Analyst: Interprets data, identifies patterns
  - Researcher: Queries knowledge graph and vector DB for context
  - Reporter: Writes executive-level briefings
  - QA: Validates outputs for accuracy
- Technology: LangGraph for orchestration, Claude API for reasoning

**Prototype Phase (Week 10, Days 3-7)**
- Build individual agents as functions
- Test each agent independently
- Chain agents: Collector → Analyst → Researcher → Reporter → QA

**Production Phase (Week 11)**
- Implement LangGraph state machine
- Add RAG (retrieval-augmented generation) using vector DB
- Create user interface for submitting queries
- Deploy as Docker container with API
- Test with complex scenarios:
  - "Analyze recent ransomware activity targeting U.S. healthcare"
  - "Generate threat profile for APT29"

**Deliverables:**
- GitHub repo with agent code, LangGraph definition
- Demo video showing multi-step reasoning
- Blog: "Why Multi-Agent Systems Are the Future of CTI"

---

### Project 5: Detection Engineering Agent
**Timeline:** Week 12
**Value:** Directly applicable to detection engineer roles

**Design Phase (Days 1-2)**
- Input: Natural language description of threat behavior
- Output: Sigma rules, Wazuh rules, KQL queries, Python detection logic
- Test environment: Wazuh SIEM for validation

**Prototype Phase (Days 3-4)**
- Build LLM agent with prompt engineering
- Test with MITRE ATT&CK techniques (T1021.001: RDP lateral movement)
- Validate generated rules in Wazuh

**Production Phase (Days 5-7)**
- Add multi-format support (Sigma, KQL, Splunk SPL)
- Create library of validated rules
- Build web interface for rule generation
- Deploy and document

**Deliverables:**
- GitHub repo with rule generator, test cases
- Library of 50+ validated detection rules
- Demo showing rule generation and testing

---

## Part 7: Cost Breakdown

### One-Time Costs
| Item | Cost | When | Required? |
|------|------|------|-----------|
| GitHub Copilot | $10/mo | Week 1 | Optional (highly recommended) |
| Domain (furywrenlabs.io) | $12/yr | Later | No (delay until Month 6) |
| Parallels Desktop | $99/yr | Week 2 | No (use free UTM instead) |
| **Total One-Time** | **$10-$120** | | |

### Monthly Recurring Costs
| Item | Cost | When | Required? |
|------|------|------|-----------|
| OpenAI API | $20/mo | Week 1 | Yes (or Claude API) |
| Hostinger VPS (n8n) | $0 | Now | No (already have) |
| AWS (beyond free tier) | $20/mo | Week 6 | Yes |
| GitHub Copilot | $10/mo | Week 1 | Optional |
| **Total Monthly** | **$30-$50** | | |

### Learning Resources
| Item | Cost | When | Required? |
|------|------|------|-----------|
| Udemy: Python for Security | $15 | Week 2 | Optional |
| Udemy: Docker Mastery | $15 | Week 1 | Optional |
| LangChain Academy (free) | $0 | Week 4 | Yes |
| Neo4j GraphAcademy (free) | $0 | Week 8 | Yes |
| AWS Free Tier Tutorials | $0 | Week 6 | Yes |
| **Total Learning** | **$0-$30** | | |

### Total 90-Day Budget
- **Minimum:** $90 (APIs only)
- **Recommended:** $300 (APIs + GitHub Copilot + courses)
- **Maximum:** $500 (all optional tools)

**Critical:** You can do this entire transition for under $100 if needed. The expensive part isn't tools—it's time investment.

---

## Part 8: Weekly Task Breakdown (Weeks 1-12)

### Week 1: Foundation
**Mon-Tue:** Docker, Python basics, first AI agent
**Wed-Thu:** Vector databases, n8n introduction
**Fri-Sun:** Home lab planning, 5 job applications
**Hours:** 40 hours
**Output:** 3 GitHub projects, 2 LinkedIn posts

### Week 2: Python for Security
**Mon-Tue:** Pandas, PCAP analysis
**Wed-Thu:** Jupyter notebooks, visualizations
**Fri-Sun:** PCAP Analysis Toolkit project
**Hours:** 35 hours
**Output:** GitHub project, technical blog post

### Week 3: API Development
**Mon-Tue:** FastAPI tutorial, REST design
**Wed-Thu:** Build Threat Intel API
**Fri-Sun:** Docker deployment, documentation
**Hours:** 35 hours
**Output:** Production API, demo video

### Week 4: Production Agent #1
**Mon-Wed:** Build Alert Triage Agent
**Thu-Fri:** Testing, refinement
**Sat-Sun:** Deploy, document, apply to 10 jobs
**Hours:** 40 hours
**Output:** Major portfolio piece, job applications

### Week 5: OSINT Pipeline
**Mon-Tue:** n8n workflows for collection
**Wed-Thu:** PostgreSQL setup, data modeling
**Fri-Sun:** Streamlit interface, testing
**Hours:** 35 hours
**Output:** OSINT Aggregation Platform

### Week 6: IOC Automation
**Mon-Tue:** n8n enrichment workflows
**Wed-Thu:** Multi-API integration
**Fri-Sun:** Vector DB integration, reporting
**Hours:** 35 hours
**Output:** Autonomous IOC Processor

### Week 7: Geopolitical Intelligence
**Mon-Wed:** GDELT/ACLED integration
**Thu-Fri:** LLM correlation logic
**Sat-Sun:** Daily briefing generator
**Hours:** 35 hours
**Output:** Geo-Cyber Intelligence Hub

### Week 8: Knowledge Graph
**Mon-Tue:** Neo4j setup, schema design
**Wed-Thu:** Data ingestion, MITRE ATT&CK import
**Fri-Sun:** Query interface, testing
**Hours:** 35 hours
**Output:** Threat Intel Knowledge Graph

### Week 9: Multi-Agent System
**Mon-Wed:** LangGraph learning, agent design
**Thu-Fri:** Agent implementation
**Sat-Sun:** Orchestration, testing
**Hours:** 40 hours
**Output:** Multi-Agent CTI System

### Week 10: Advanced Agents
**Mon-Wed:** RAG implementation
**Thu-Fri:** Context retrieval optimization
**Sat-Sun:** Polish multi-agent system
**Hours:** 35 hours
**Output:** Enhanced CTI system with RAG

### Week 11: Detection Agent
**Mon-Tue:** Detection rule generation agent
**Wed-Thu:** Validation in Wazuh
**Fri-Sun:** Rule library creation
**Hours:** 30 hours
**Output:** AI Detection Engineer tool

### Week 12: Portfolio Finalization
**Mon-Wed:** Polish all GitHub repos
**Thu-Fri:** Create demo videos, write case studies
**Sat-Sun:** Portfolio site (GitHub Pages), apply to 20 jobs
**Hours:** 35 hours
**Output:** Complete portfolio, 20 applications

**Total Hours:** 420 hours over 90 days (avg 35 hours/week, very aggressive)

---

## Part 9: Daily Schedule Template

### Optimal Schedule for Aggressive Transition (Mon-Fri)
**5:00 AM - 7:00 AM:** Deep work (coding, no distractions)
**7:00 AM - 8:00 AM:** Break, exercise, breakfast
**8:00 AM - 12:00 PM:** Main project work (building)
**12:00 PM - 1:00 PM:** Lunch, short walk
**1:00 PM - 3:00 PM:** Learning (tutorials, reading docs)
**3:00 PM - 4:00 PM:** Break
**4:00 PM - 6:00 PM:** Testing, documentation, GitHub
**6:00 PM - 7:00 PM:** Networking (LinkedIn posts, job applications)
**Evening:** Family time, rest

**Total:** 8-9 hours/day on transition

### Weekend Schedule
**Sat:** 6 hours (polish projects, write blog posts)
**Sun:** 4 hours (review week, plan next week, light learning)

**Critical:** This is aggressive. Adjust based on your energy and other commitments. Consistency matters more than intensity.

---

## Part 10: Key Decisions

### 1. Website Priority: DELAY UNTIL MONTH 6
**Reasoning:**
- Recruiters at CrowdStrike, Google, Anthropic prioritize GitHub over personal sites
- Building a good site takes 40+ hours (better spent on projects)
- GitHub README as portfolio is sufficient for first 90 days
- Revisit after you have 8-10 solid projects

**Action:** Use GitHub profile README as your "site" for now. Add furywrenlabs.io later when you have content to showcase.

---

### 2. Loveable Platform: OPTIONAL, LOW PRIORITY
**Reasoning:**
- Loveable is great for rapid UI prototyping
- Your core skill gap is backend (Python, APIs, agents), not frontend
- Time spent on UI design doesn't differentiate you for AI/security roles

**Action:** Use Streamlit (Python-based, simpler) for quick UIs. Consider Loveable only if you have extra time in Weeks 10-12 and want to polish a specific project.

---

### 3. n8n Hosting: LOCAL + HOSTINGER VPS
**Recommendation:**
- **Local n8n** (Docker on MacBook or NAS): Development and testing
- **Hostinger VPS n8n**: Production workflows (threat intel collection, automated briefings)

**Reasoning:** Demonstrates cloud deployment while keeping dev environment isolated.

---

### 4. Certifications: SKIP FOR NOW
**Reasoning:**
- Your 15 years of intelligence experience >> entry-level certs
- Roles you're targeting care about GitHub portfolio and practical skills
- Consider Security+ only if job postings require it (unlikely for senior roles)

**Action:** Focus 100% on building. Certifications are checkbox items for HR, not hiring managers at Google or CrowdStrike.

---

### 5. Email: Use jaygulyash@gmail.com FOR NOW
**Reasoning:**
- jgulyash@furywrenlabs.io looks professional but isn't critical yet
- Switching emails mid-job-search is confusing
- Gmail is trusted for deliverability

**Action:** Set up furywrenlabs.io email in Month 6 when launching website. Forward it to Gmail.

---

## Part 11: Job Application Strategy

### Week 1-4: Target 20 Applications
**Focus:** Early feedback on resume and portfolio

**Companies:**
- Google Mandiant, CrowdStrike, Recorded Future, Cloudflare, Microsoft, Palo Alto Networks, Splunk, Elastic, Datadog, Wiz

**Roles:**
- Cyber Threat Intelligence Analyst (AI-focused)
- Security Engineer (Detection)
- Threat Intelligence Engineer

**Resume Strategy:**
- Emphasize 15 years of intel tradecraft
- Add "Personal Projects" section with GitHub links (even if projects are basic in Week 1)
- Customize for each company (mention their products/technologies)

---

### Week 5-8: Target 30 Applications
**Focus:** Leverage growing portfolio

**Additional Companies:**
- Anthropic, OpenAI, Anduril, Palantir, Scale AI, Snyk, Abnormal Security, Huntress, Expel, Red Canary

**Roles:**
- Security AI/ML Engineer
- Detection Engineering Lead
- Security Automation Engineer

**Strategy:**
- Link to specific GitHub projects in cover letter
- Create demo videos and embed in applications
- Cold outreach on LinkedIn to hiring managers with portfolio

---

### Week 9-12: Target 30+ Applications
**Focus:** Aggressive push with complete portfolio

**Additional Companies:**
- Startups (10a Labs, stealth mode companies)
- VC-backed security firms (check Crunchbase)
- Consulting firms (Mandiant/Google Cloud, KPMG, Deloitte Cyber)

**Roles:**
- AI Agent Engineer (Security)
- Principal Security Engineer
- AI Solutions Architect (Security)

**Strategy:**
- Portfolio site live (GitHub Pages)
- Case studies for top 3 projects
- Cold email CEOs/CTOs at startups (your background is extremely relevant)
- Leverage LinkedIn content (should have 10+ posts by now)

---

## Part 12: Upskilling Resources (Free & Low-Cost)

### Python (Weeks 1-4)
- **Automate the Boring Stuff with Python** (free online book)
- **Real Python** (freemium, excellent tutorials)
- **Udemy: Python for Cybersecurity** ($15, optional)

### Docker (Weeks 1-2)
- **Docker's Official Tutorial** (free)
- **TechWorld with Nana (YouTube)** (free)

### AI Agents (Weeks 3-10)
- **LangChain Academy** (free, comprehensive)
- **DeepLearning.AI: LangChain for LLM Application Development** (free on Coursera with audit)
- **LangGraph Documentation** (free)

### Vector Databases (Weeks 5-6)
- **Chroma Documentation** (free)
- **Pinecone Learning Center** (free)
- **Weaviate Academy** (free)

### Knowledge Graphs (Week 8)
- **Neo4j GraphAcademy** (free, excellent)
- **Graph Data Science Fundamentals** (free course)

### n8n Automation (Weeks 5-7)
- **n8n Documentation** (free)
- **n8n YouTube Channel** (free tutorials)

### Detection Engineering (Ongoing)
- **Sigma Rules Repository** (free, study examples)
- **MITRE ATT&CK Navigator** (free)
- **Florian Roth's Blog** (free, excellent detection content)

---

## Part 13: Red Flags to Avoid

### 1. Tutorial Hell
**Problem:** Watching endless tutorials without building
**Solution:** 80% building, 20% learning. If you spend more than 1 hour on a tutorial, immediately apply it in a project.

### 2. Over-Engineering
**Problem:** Spending weeks perfecting one project
**Solution:** Ship early, iterate later. A working prototype is better than a perfect design doc.

### 3. Isolation
**Problem:** Building in a vacuum without feedback
**Solution:** Post weekly updates on LinkedIn. Join Discord communities (LangChain, Wazuh, etc.). Ask for feedback on GitHub.

### 4. Analysis Paralysis
**Problem:** Researching "best practices" instead of building
**Solution:** Pick a tool and start. You can always refactor. Done is better than perfect.

### 5. Shiny Object Syndrome
**Problem:** Chasing new frameworks instead of finishing projects
**Solution:** Stick to the roadmap. Finish 3 projects before exploring new tools.

---

## Part 14: Success Metrics

### 30-Day Goals (End of Week 4)
- [ ] 3 GitHub projects with working code
- [ ] 1 production-ready AI agent (Alert Triage System)
- [ ] 5 LinkedIn posts showing progress
- [ ] 20 job applications submitted
- [ ] Docker proficiency: Can deploy multi-container apps
- [ ] Python proficiency: Can write scripts without constant Googling

### 60-Day Goals (End of Week 8)
- [ ] 6 GitHub projects
- [ ] Intelligence Automation Hub operational
- [ ] Threat Intel Knowledge Graph deployed
- [ ] 10 LinkedIn posts, growing network
- [ ] 50 job applications submitted
- [ ] First interview requests (likely informational, not job offers yet)

### 90-Day Goals (End of Week 12)
- [ ] 8-10 production-grade projects on GitHub
- [ ] Complete portfolio with case studies
- [ ] 80 job applications submitted
- [ ] 3-5 active interview processes
- [ ] Technical depth: Can explain agent architectures, vector databases, detection engineering
- [ ] Community presence: Known in LangChain/security Discord, regular LinkedIn contributor

### 180-Day Goals (Exit Criteria)
- [ ] Job offer at $165k+ from target company
- [ ] 5+ projects with active users or community interest
- [ ] Speaking/writing opportunities (conference talks, blog guests)
- [ ] Consulting opportunities (side income while job searching)

---

## Part 15: Contingency Plans

### Scenario 1: Not Getting Interviews After 60 Days
**Diagnosis:** Resume or portfolio not resonating
**Fix:**
- Get resume review from someone at target company (LinkedIn cold outreach)
- Create 2-minute video intro showcasing top project (more engaging than text)
- Apply to smaller companies (Series A/B startups more open to career changers)
- Consider contract roles (easier entry, often convert to full-time)

### Scenario 2: Overwhelmed by Technical Complexity
**Diagnosis:** Moving too fast, gaps in fundamentals
**Fix:**
- Slow down to 3-4 hours/day instead of 8
- Focus on one technology at a time (e.g., just Python for 2 weeks)
- Find a mentor (post on r/cybersecurity, r/MachineLearning asking for guidance)
- Pair with another learner (accountability partner)

### Scenario 3: Running Out of Money
**Diagnosis:** Budget exceeded, need to reduce costs
**Fix:**
- Use Claude API instead of OpenAI (likely cheaper for your use case)
- Use local LLMs (Ollama, GPT4All) instead of paid APIs
- Pause AWS, use only local infrastructure
- **Total monthly cost can drop to $0 if needed**

### Scenario 4: Prototyping Takes Too Long
**Diagnosis:** Perfectionism or scope creep
**Fix:**
- Timebox each project: 7 days max per project
- Use templates (GitHub has LangChain agent templates)
- Embrace "good enough" mindset for v1
- Ship, then iterate based on feedback

---

## Part 16: Immediate Next Steps (Today)

### Action Plan (Next 4 Hours)

**Hour 1: Environment Setup**
- [ ] Install VS Code, Docker Desktop, Python (via pyenv)
- [ ] Create GitHub account (if don't have) and repository: `furywren-ai-lab`
- [ ] Update LinkedIn headline: "Senior Threat Intelligence Analyst | Transitioning to AI-Powered Security Engineering"

**Hour 2: First Python Script**
- [ ] Write script that parses a list of IPs from a text file
- [ ] Print each IP with a label: "IP: 1.2.3.4"
- [ ] Push to GitHub with README

**Hour 3: First Docker Container**
- [ ] Create Dockerfile for Python script
- [ ] Build image: `docker build -t ip-parser .`
- [ ] Run container: `docker run ip-parser`
- [ ] Document in README

**Hour 4: First Job Applications**
- [ ] Update resume to add "Personal Projects" section with GitHub link
- [ ] Apply to: Google Mandiant, CrowdStrike, Recorded Future
- [ ] Customize cover letters mentioning your intel background + AI transition

**Output:** By end of today, you'll have:
- Working dev environment
- First GitHub commit
- First Docker container
- 3 job applications submitted

---

## Final Thoughts

**You have a rare combination:** Deep intelligence tradecraft + operational experience + genuine interest in AI. Most AI engineers don't understand threat intelligence. Most threat analysts don't code. You're bridging both worlds, which is exactly what companies like Google Mandiant, CrowdStrike, and Anthropic need.

**Your unfair advantage:** You can speak the language of both security analysts and data scientists. You understand the "why" behind detection engineering (because you've hunted real threats) and the "how" of AI systems (because you're building them). This is a 10x multiplier in a market desperate for this hybrid skill set.

**The market reality:** AI security roles are growing faster than talent pools. Companies are hiring people with adjacent experience and upskilling them. Your resume screams "we can teach them to code better, but we can't teach threat intuition."

**The key to success:** Ship working code every week. Consistency beats intensity. One project per week for 12 weeks is more impressive than one perfect project in 12 weeks.

**Don't build the website yet.** Build your GitHub portfolio. That's your real estate for the next 90 days. The website can wait until you have something worth showcasing.

**Start today.** Not tomorrow. Not after more planning. Follow the 4-hour action plan above right now. Momentum is everything in career transitions.

---

## Appendix: Recommended Tools Stack

### Must-Have (Free)
- **Python** (programming language)
- **Docker** (containerization)
- **VS Code** (IDE)
- **Git/GitHub** (version control)
- **LangChain** (agent framework)
- **Chroma** (vector database)
- **Streamlit** (UI framework)
- **n8n** (automation)
- **Wazuh** (SIEM)
- **Suricata** (IDS)
- **PostgreSQL** (database)
- **Neo4j** (knowledge graph)

### Highly Recommended ($)
- **GitHub Copilot** ($10/month) - 10x coding speed
- **Claude API** ($20/month) - Better for reasoning than GPT-3.5
- **AWS** ($20/month) - Cloud deployment experience

### Optional/Later
- **Qdrant Cloud** (hosted vector DB, free tier available)
- **Pinecone** (alternative to Chroma, $70/month for production)
- **Hostinger VPS** (already have for n8n)
- **Domain** (furywrenlabs.io, delay until month 6)

---

**Ready to start? Begin with Day 1, Hour 1. Everything else follows from that first commit.**

Let's build your AI security engineering career. One Docker container at a time.
