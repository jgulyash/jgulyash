# FuryWren Labs - AI-Powered Security Engineering

**Jay Gulyash** | Senior Threat Intelligence Analyst → AI Security Engineer

Bridging 15 years of intelligence tradecraft with AI-native security engineering. Building production-grade threat detection systems, autonomous intelligence agents, and security automation workflows.

## 🚀 What I'm Building

This repository showcases my transition from traditional threat intelligence to AI-powered security engineering through hands-on projects deployed in my home lab.

**Focus Areas:**
- 🤖 AI agents for threat intelligence and detection engineering
- 🔍 Automated OSINT collection and analysis pipelines
- 🛡️ Security automation workflows using n8n and LangChain
- 📊 Knowledge graphs for threat actor attribution and TTP mapping
- 🎯 Production-ready security tools, not just prototypes

## 📂 Navigation

- **[AI Engineer Transition Plan](./AI-ENGINEER-TRANSITION-PLAN.md)** - Comprehensive 90-day roadmap from beginner to production AI security engineer
- **[Projects](#projects)** - Working demos of AI security systems
- **[Lab Architecture](#lab-architecture)** - Home lab infrastructure and network design
- **[Contact](#connect)** - Let's connect

## Current Status

**Phase:** Foundation (Week 1 of 90-day plan)
**Focus:** Python fundamentals, Docker, first AI agent

### Tech Stack
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![Neo4J](https://img.shields.io/badge/Neo4j-008CC1?style=for-the-badge&logo=neo4j&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgresql-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Wazuh](https://img.shields.io/badge/Wazuh-000000?style=for-the-badge&logo=wazuh&logoColor=white)
![Suricata](https://img.shields.io/badge/Suricata-FF3300?style=for-the-badge&logo=suricata&logoColor=white)

---

## Projects

### 🎯 Completed
*Building in progress - check back soon*

### 🚧 In Development
1. **IOC Enrichment Agent** - Python script + AI agent for automated threat intelligence lookups
2. **Home Lab Infrastructure** - Dockerized security stack (Wazuh, Suricata, MISP)

### 📋 Planned (Next 90 Days)
- AI-Powered Alert Triage System
- Intelligence Automation Hub (n8n + LangChain)
- Threat Intelligence Knowledge Graph (Neo4j)
- Multi-Agent CTI System (LangGraph)
- Detection Engineering Agent (Auto-generate SIEM rules)

See the [full roadmap](./AI-ENGINEER-TRANSITION-PLAN.md) for details.

---

## Lab Architecture

**FuryWren Labs** - Enterprise-Grade Home Lab

### Hardware
- **Primary Host:** MacBook Pro M4 (14-core CPU, 32-core GPU, 36GB RAM)
- **Storage/Services:** Synology DS1522+ NAS (32GB RAM, 20TB storage)
- **Client/Testing:** MacBook Air M2 (16GB RAM)
- **Security:** Protectli VP2430 (OPNsense firewall, 32GB RAM, 500GB SSD)
- **Monitoring:** Raspberry Pi 5 (Suricata IDS)
- **Network:** NETGEAR GS108Ev4 switch, GigaSpire BLAST router

### Network Design
```
Internet
    ↓
[ISP Router] (192.168.1.0/24)
    ↓
[Protectli OPNsense] (Firewall/VPN/IDS)
    ↓
    ├─ Lab Network (10.0.10.0/24)
    │   ├─ MacBook M4 (Development)
    │   ├─ Synology NAS (Docker containers)
    │   ├─ MacBook M2 (Testing)
    │   └─ Raspberry Pi (Suricata monitoring)
    └─ Home Network (Isolated)

[TwinGate] → Secure remote access to lab
```

### Containerized Services (Synology NAS)
- **Wazuh SIEM/XDR** - Threat detection and monitoring
- **MISP** - Threat intelligence platform
- **PostgreSQL** - Data storage
- **Qdrant** - Vector database for AI agents
- **Neo4j** - Knowledge graph (planned)
- **n8n** - Automation workflows

See [detailed setup guide](./AI-ENGINEER-TRANSITION-PLAN.md#part-5-home-lab-setup-guide) for implementation.

---

## Skills Being Developed

**AI Engineering (65%)**
- Python programming for security automation
- LangChain/LangGraph for multi-agent systems
- Vector databases (Chroma, Qdrant) and RAG architecture
- FastAPI for building security APIs
- Docker/containerization for deployment
- Knowledge graphs with Neo4j

**Cyber Threat Intelligence (35%)**
- SIEM detection engineering (Wazuh, Sigma rules)
- Automated OSINT collection and correlation
- Threat actor attribution and TTP mapping
- IOC enrichment and analysis
- Security automation workflows (n8n)
- Network security monitoring (Suricata, OPNsense)

---

## Why This Matters

I'm not just learning AI - I'm applying it to solve real security problems using 15 years of threat intelligence tradecraft. Every project demonstrates:

1. **Practical Security Value** - Solves actual problems SOC analysts face
2. **Production Quality** - Deployed and tested, not just proof-of-concepts
3. **AI-Native Approach** - Uses modern agent frameworks and LLMs
4. **Enterprise Relevance** - Built with tools companies actually use

**Target Roles:** AI-Powered Threat Intelligence Engineer | Security AI/ML Engineer | Detection Engineering Lead

---

## 📈 Progress Tracking

**90-Day Aggressive Transition Plan: Week 1 of 12**

- [x] Career roadmap defined
- [x] Home lab architecture designed
- [ ] First Python script (IOC parser)
- [ ] First Docker container deployed
- [ ] First AI agent (IOC enrichment)
- [ ] 5 job applications submitted

[View detailed roadmap →](./AI-ENGINEER-TRANSITION-PLAN.md)

---

## 🎯 Target Companies

**Tier 1:** Google Mandiant, CrowdStrike, Recorded Future, Anthropic, Cloudflare, OpenAI
**Tier 2:** Microsoft, Palo Alto Networks, Splunk, Elastic, Wiz, Datadog
**Tier 3:** Startups (10a Labs, stealth-mode AI security companies)

**Target Role:** Remote-only, $165k+, 65% AI Engineering + 35% Threat Intel

---

## Connect

**Jay Gulyash**
Senior Threat Intelligence Analyst | Building AI-Powered Security Systems

- **LinkedIn:** [linkedin.com/in/jay-gulyash-750489207](https://www.linkedin.com/in/jay-gulyash-750489207)
- **Email:** jaygulyash@gmail.com
- **Location:** Colorado (Remote, up to 25% travel)

*Currently in active job search - open to opportunities starting Q1 2026*

---

## License

This repository is licensed under the MIT License. See [LICENSE](./LICENSE) for details.

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
