![EpicStaff Logo](logo.png)
   
# EpicStaff: Open-Source Multi-Agent Orchestration Platform

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
  <a href="#key-features">Features</a> •
  <a href="https://github.com/EpicStaff/EpicStaff/issues">Report Bug</a>
</div>

  <p align="center">
    <b>Open-Source Hybrid AI Agent Orchestrator</b>
    <br />
    Bridge the gap between visual workflow builders and pure-code AI frameworks.
     <div align="center">
   
Our core philosophy: **We hide the complexity, not the logic.**

**⭐ Star us on GitHub to support the project and follow our progress!**
</div>

---
 <p align="center">
    
## 📺 Watch it in Action

![Watch the EpicStaff Demo](https://github.com/EpicStaff/EpicStaff-resources/blob/main/how_to_create_flow.gif?raw=true)
</div>
    
---

## Why EpicStaff?

Most tools force a trade-off: simplicity (No-Code) vs. flexibility (Code-First). **EpicStaff** eliminates this barrier by providing a **Visual + Code hybrid environment**.

It is a high-performance orchestration platform designed to allow developers to build, deploy, and scale multi-agent systems without losing control over the underlying logic.

* **Visual Logic, Python Core:** Design flows in a node-based editor; inject custom Python logic directly into any node.
* **Production-Ready Persistence:** Built-in state management for user and organization variables.
* **Solid Backend Foundation:** Powered by **Django** for robust data management and security.

---

## ⚡ Quick Start

You don't need to be a technical expert to launch EpicStaff. Follow these two simple steps to get the application running on your computer.

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

### Once running, open http://localhost:4200 to start building.

### Alternative Setup Options

EpicStaff can be configured and launched using alternative setup methods:

- **[Partly Local Setup](https://github.com/EpicStaff/EpicStaff/blob/main/partly-local-setup.md)** — run specific services locally while other services remain in Docker. Useful for controlled local development and testing.  
- **[Podman Support](https://github.com/EpicStaff/EpicStaff/blob/main/podman-setup.md)** — provides instructions for deploying EpicStaff using **Podman** instead of Docker.

> These methods are optional and intended for users requiring advanced control over their environment.

**For more [details](https://github.com/EpicStaff/EpicStaff/wiki)**

---

## Key Features

| Feature | Technical Description |
| :--- | :--- |
| **Hybrid Execution Engine** | Combines visual graph traversal (DAG) with direct Python code injection. Code nodes run in isolated Docker containers. |
| **Dual-Layer Memory** | **Short-term:** Configurable "Window Memory" for conversation context. <br> **Long-term:** Persistent variables stored in PostgreSQL at the User or Organization level. |
| **Integrated RAG (Knowledge)** | Upload documents, auto-chunk text, and attach vector-based **Knowledge Bases** directly to agents without external DB setup. |
| **Human Input** | Native **Human-in-the-Loop** capability. Pauses flow execution to wait for operator feedback or approval before proceeding. |
| **Real-Time Streaming** | Native support for **Server-Sent Events (SSE)**. Stream agent reasoning, tool outputs, and chat responses instantly to the UI. |
| **Secure Sandboxing** | File system access is restricted to defined volume paths (`CONTAINER_SAVEFILES_PATH`). Custom tools operate within strict boundaries. |
| **Multi-Model Routing** | Native support for switching between OpenAI, Anthropic, and local LLMs (Ollama/LocalLLaMA) within the same flow. |

---

## Join Our Community & Shape the Future of EpicStaff

EpicStaff is an open-source project driven by its community. Whether you're a developer, a no-code enthusiast, or a business professional, your feedback and contributions are what make this project grow.

* **⭐ Star the Repository:** The easiest way to show your support and stay updated.
* **💬 Connect on Reddit:** For real-time chat with the community and the core team, join our [Reddit Community](https://www.reddit.com/r/EpicStaff_AI/). 
* **🤝 Contribute:** Found a bug or want to add a new tool? Check out our [CONTRIBUTING.md](CONTRIBUTING.md) to get started. We welcome all contributors!

**Let's build the future of intelligent, collaborative systems together!**

## 🙏 Special Thanks

Our platform leverages the innovative work of the open-source community. A special thank you goes out to **[Foblex](https://github.com/Foblex)** for their collaboration and fantastic contributions.

* We proudly use the **[f-flow library](https://github.com/Foblex/f-flow)** which is a core part of our architecture.
* Foblex helps us spread the word by featuring EpicStaff in his articles and educational materials. You can check out his work at **[flow.foblex.com](https://flow.foblex.com/)**.

We believe in the power of collaboration and are grateful for such a great partnership.

