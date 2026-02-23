![EpicStaff Logo](logo.png)

   <div align="center">  
      
# EpicStaff: Enterprise Workflow Automation & AI Agent Management Platform
 Open Source Agent Orchestration Framework for Django & Python
</div>

<a id="readme-top"></a>

<div align="center">  
   
[![GitHub Stars](https://img.shields.io/github/stars/EpicStaff/EpicStaff?style=social)](https://github.com/EpicStaff/EpicStaff/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/EpicStaff/EpicStaff?style=social)](https://github.com/EpicStaff/EpicStaff/network/members)
[![License](https://img.shields.io/github/license/EpicStaff/EpicStaff)](https://github.com/EpicStaff/EpicStaff/blob/main/LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/EpicStaff/EpicStaff)](https://github.com/EpicStaff/EpicStaff/commits/main)
[![Open Issues](https://img.shields.io/github/issues/EpicStaff/EpicStaff)](https://github.com/EpicStaff/EpicStaff/issues)

</div>

<p align="center">
<br />
  <a href="https://www.epicstaff.ai">Website</a> •
  <a href="https://github.com/EpicStaff/EpicStaff/wiki">Wiki</a> •
  <a href="#-quick-start">Quick Start</a> •
  <a href="#key-features">Key Features</a> •
  <a href="https://github.com/EpicStaff/EpicStaff/issues">Report Bug</a>
</div>

  <p align="center">
    <b>Production-Grade Agentic UI for Multi-Agent Orchestration</b>
    <br />
EpicStaff is an Enterprise-ready Agentic UI platform that simplifies multi-agent orchestration by hiding complexity behind a visual workflow builder while maintaining full code control with a Django backend.
     <div align="center">
   
Our core philosophy: **We hide the complexity, not the logic.**

**⭐ Star us on GitHub to support the Agentic UI movement!**
</div>

---
 <p align="center">
    
## 📺 Visual Agent Orchestrator in Action

![Watch the EpicStaff Demo](https://github.com/EpicStaff/EpicStaff-resources/blob/main/how_to_create_flow.gif?raw=true)
</div>
    
---

## Why did we create EpicStaff?

Most tools force a trade-off: simplicity (No-Code) vs. flexibility (Code-First). **EpicStaff** eliminates this barrier by providing a **Visual + Code** hybrid environment.

It is a high-performance orchestration platform designed to allow developers to build, deploy, and scale multi-agent systems without losing control over the underlying logic.

* **Visual Logic, Python Core:** Design flows in a drag-and-drop AI workflow editor; inject custom Python logic directly into any node.
* **Cross-Flow Agent Context:** Built-in persistent agent memory (Redis/PostgreSQL) to retain context across multiple sessions.
* **Production-Ready Persistence:** Built-in state management for user and organization variables.
* **Django Multi-Agent Backend:** Powered by Django for robust, low-latency, and production-ready Pythonic agent orchestration.

---

## ⚡ Quick Start

Deploy self-hosted AI agents in 30 seconds. EpicStaff is designed to run securely on your own infrastructure.
Follow these two simple steps to get the application running on your computer.

### Step 1: Get the necessary tools
Before we start, make sure you have these two applications installed:
* **[Download & Install Git](https://git-scm.com/downloads)** (Required to download the app)
* **[Download & Install Docker Desktop](https://www.docker.com/products/docker-desktop/)** (Required to run the app)

### Step 2: Download and Setup
Choose your operating system below, open your **Terminal** (or PowerShell on Windows), and **paste the entire block of code**. This command will automatically download EpicStaff, configure the database, and start the system.

#### 🪟 Windows (PowerShell)
```
git clone [https://github.com/EpicStaff/EpicStaff.git](https://github.com/EpicStaff/EpicStaff.git); cd EpicStaff/src; $savefiles = "$HOME/savefiles"; $file = ".env"; (Get-Content $file) -replace "CREW_SAVEFILES_PATH=/c/savefiles", "CREW_SAVEFILES_PATH=$savefiles" | Set-Content $file; docker volume create sandbox_venvs; docker volume create sandbox_executions; docker volume create crew_pgdata; docker volume create crew_config; docker volume create media_data; docker network create mcp-network; docker-compose up --build
```
#### 🍎 macOS (Terminal)
```
git clone -b main [https://github.com/EpicStaff/EpicStaff.git](https://github.com/EpicStaff/EpicStaff.git) && cd EpicStaff && savefiles="$HOME/savefiles" && sed -i '' "s|CREW_SAVEFILES_PATH=/c/savefiles|CREW_SAVEFILES_PATH=$savefiles|" src/.env && docker volume create sandbox_venvs && docker volume create sandbox_executions && docker volume create crew_pgdata && docker volume create crew_config && docker volume create media_data && docker network create mcp-network && cd src && docker-compose up --build
```
#### 🐧 Linux (Terminal)
```
git clone -b main [https://github.com/EpicStaff/EpicStaff.git](https://github.com/EpicStaff/EpicStaff.git) && cd EpicStaff && savefiles="$HOME/savefiles" && sed -i "s|CREW_SAVEFILES_PATH=/c/savefiles|CREW_SAVEFILES_PATH=$savefiles|" src/.env && docker volume create sandbox_venvs && docker volume create sandbox_executions && docker volume create crew_pgdata && docker volume create crew_config && docker volume create media_data && docker network create mcp-network && cd src && docker-compose up --build
```

Once running, open http://localhost:4200 to start building.

<details>
<summary>Alternative Setup Options</summary>

EpicStaff can be configured and launched using alternative setup methods:

- **[Partly Local Setup](https://github.com/EpicStaff/EpicStaff/blob/main/partly-local-setup.md)** — run specific services locally while other services remain in Docker. Useful for controlled local development and testing.  
- **[Podman Support](https://github.com/EpicStaff/EpicStaff/blob/main/podman-setup.md)** — provides instructions for deploying EpicStaff using **Podman** instead of Docker.

> These methods are optional and intended for users requiring advanced control over their environment.

**For more [details](https://github.com/EpicStaff/EpicStaff/wiki)**
</details>

---

## Key Features 

<details>
<summary>Key features For AI Engineers</summary>

We built a foundation for robust ai agent orchestration and Open Source Agent Orchestration. You can design ai agent orchestration for complex workflows and deploy autonomous AI agents with complete control over the execution logic. The architecture natively supports creating a dependable rag pipeline and managing advanced RAG workflows without external vector database dependencies. For developers exploring the code, we ensure stable execution to prevent the notorious ralph wiggum loop, and you might even spot a ralph wiggum github reference in our test repositories.

| Feature | Technical Description |
|---|---|
| Agentic UI Framework | A low-code, drag-and-drop AI workflow builder that combines visual graph traversal (DAG) with isolated Python execution environments. |
| Persistent Agent Memory | Dual-Layer Memory: Short-term window context + Long-term stateful memory across multiple sessions, stored in PostgreSQL/Redis. |
| Low-code GraphRAG | Fix RAG hallucinations in agents. Auto-chunk text and attach vector-based knowledge directly to agents without external DB setup. |
| Human-in-the-Loop UI | Enterprise-grade flow control. Pause multi-agent orchestration to wait for human operator feedback or validation before proceeding. |
| Agent Reasoning Trace | Debug multi-agent workflows effortlessly. Native SSE streaming provides a real-time visual trace of how your agent "thinks" and uses tools. |
| Secure Sandboxing | File system access is restricted (`CONTAINER_SAVEFILES_PATH`). Custom Python tools operate within strict Docker boundaries. |
| Multi-Model Routing | Seamlessly switch between OpenAI, Anthropic, and local LLMs (Ollama/LocalLLaMA) dynamically within the same workflow. |
</details>

---

<details>
<summary>Key Features For Business</summary>

As an ai agent management platform, EpicStaff is engineered to deliver enterprise workflow automation and scalable business process automation. It functions as an Autonomous Agent Builder that acts as a drag and drop automation tool for cross-functional teams. By utilizing sophisticated ai workflow management and built-in ai agent assist, organizations can drastically improve their AI CX (ai customer experience). Being a versatile low code platform, it bridges the gap between technical operations and business strategy.

| Feature | Strategic Business Value |
|---|---|
| Natural Language to SQL | Enables business users to instantly retrieve metrics from MySQL and PostgreSQL databases using plain English, removing the dependency on data analysts. |
| Human Input Control | Maintains human oversight over sensitive operations by pausing workflows for manual review and validation before an agent executes a final decision. |
| Knowledge Sources & Chat | Automates onboarding and standard inquiries by allowing teams to build real-time conversational agents grounded securely in internal company documents. |
| Webhook Triggers | Creates continuous automated processes where external events, such as a new CRM entry, instantly trigger an agent to analyze data via HTTP POST payloads. |
| Persistent Variables | Tracks complex long-term business logic for cross-functional teams, such as managing usage quotas or monitoring funnel stages across multiple workflow runs. |
| Web Scraping & Image Generation | Scales content creation and research by automatically gathering web data and generating visual assets without requiring additional operational resources. |

</details>

---

## Join Our Community & Shape the Future of EpicStaff

EpicStaff is an open-source project driven by its community. Whether you want to build custom Python tools, improve the Django backend, or design new Agentic UI components, your contributions matter!

* **⭐ Star the Repository:** Support the Agentic UI movement.
* **💬 Connect on Reddit:** For real-time chat with the community and the core team, join our [Reddit Community](https://www.reddit.com/r/EpicStaff_AI/). 
* **🤝 Contribute:** Found a bug or want to add a new tool? Check out our [CONTRIBUTING.md](CONTRIBUTING.md) to get started. We welcome all contributors!

**Let's build the future of intelligent, collaborative systems together!**

## 🙏 Special Thanks

Our visual-first agentic system leverages the innovative work of the open-source community. A special thank you to **[Foblex](https://github.com/Foblex)**

* We proudly use the **[f-flow library](https://github.com/Foblex/f-flow)** as the core interactive engine for our Agentic UI.
* Foblex helps us spread the word by featuring EpicStaff in his articles and educational materials. You can check out his work at **[flow.foblex.com](https://flow.foblex.com/)**.

We believe in the power of collaboration and are grateful for such a great partnership.

