<div align="center">

# 🚀 NitroPilot

### *The AI That Executes Your Commands*

[![Stars](https://img.shields.io/github/stars/tonivega/nitropilot?style=for-the-badge&logo=github&color=yellow)](https://github.com/tonivega/nitropilot/stargazers)
[![Go Version](https://img.shields.io/badge/Go-1.22+-00ADD8?style=for-the-badge&logo=go)](https://go.dev/)
[![Claude Sonnet 4](https://img.shields.io/badge/Powered%20by-Claude%20Sonnet%204-5A67D8?style=for-the-badge)](https://anthropic.com)

**Tell it what to do. Watch it happen.**

[🎯 Quick Start](#-quick-start) • [✨ Features](#-features) • [🎬 Demo](#-demo) • [📖 Docs](#-documentation) • [🤝 Contributing](#-contributing)


### ⚡ **20,000 Stars = Full Open Source Release**

**Help us reach 20K stars to unlock the complete source code!**

<div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); padding: 20px; border-radius: 10px; margin: 20px 0;">

### 🎁 **UNLOCK AT 20K STARS:**

**[⭐ Star Now](https://github.com/tonivega/nitropilot) | Current: ![GitHub stars](https://img.shields.io/github/stars/tonivega/nitropilot?style=social)**

</div>

</div>


## 🎯 What is NitroPilot?

**NitroPilot** is a new autonomous AI agent that transforms natural language into executed commands. Unlike traditional AI assistants that just *suggest* commands, NitroPilot **plans, executes, validates, and self-corrects** until your goal is achieved.

### 🔥 The Problem We Solve

```bash
# Traditional AI Workflow (Frustrating!)
You: "Deploy my app to production"
AI: "Here's a command you could try..."
You: *copies command*
You: *pastes command*
You: *hits enter*
Terminal: ERROR
You: *asks AI for fix*
AI: "Oh, try this instead..."
# 🔄 Repeat 10 times...
```

```bash
# NitroPilot Workflow (Effortless!)
You: "Deploy my app to production"
NitroPilot: *analyzing environment...*
NitroPilot: *executing deployment steps...*
NitroPilot: *validating each step...*
NitroPilot: *auto-fixing errors...*
NitroPilot: ✅ Deployment complete!
```


## ✨ Features

### 🧠 **Autonomous Intelligence**

### ⚡ **Developer Experience**


## 🎬 Demo

### Example 1: Automated Setup

```bash
$ nitropilot --log-json setup.jsonl \
 "Install Go 1.22, clone my repo from github.com/me/myapp, and build it"

nitropilot - nitrobutton.com
🎯 Planning: Install Go 1.22, clone repo, build...
✓ Step 1: Check Go version
✓ Step 2: Install Go 1.22 via apt
✓ Step 3: Clone repository
✓ Step 4: Build application
✅ Success! Built binary at ./myapp/bin/myapp
```

### Example 2: DevOps Automation

```bash
$ nitropilot --log-json deploy.jsonl \
 "Deploy the app to production using docker-compose, run migrations, and verify health"

🎯 Planning: Docker deployment with migrations and health checks...
✓ Step 1: Check Docker installation
✓ Step 2: Build Docker image
✓ Step 3: Run docker-compose up
✓ Step 4: Execute database migrations
✓ Step 5: Health check on http://localhost:8080/health
✅ Deployment successful! App is healthy.
```

### Example 3: Data Pipeline

```bash
$ nitropilot --log-json etl.jsonl \
 "Download sales data from S3, process with Python pandas, and upload results to PostgreSQL"

🎯 Planning: S3 download → pandas processing → PostgreSQL upload...
✓ Step 1: Check AWS credentials
✓ Step 2: Download from s3://sales-data/2024/
✓ Step 3: Run pandas ETL script
✓ Step 4: Upload to PostgreSQL
✅ Processed 1.2M records successfully!
```


## 🚀 Quick Start

### Prerequisites



### Installation

```bash
# Download latest release
curl -LO https://github.com/tonivega/nitropilot/releases/latest/download/nitropilot
chmod +x nitropilot
sudo mv nitropilot /usr/local/bin/
```

### Usage

```bash
# Set your API key
export ANTHROPIC_API_KEY='your-key-here'

# Run a command
nitropilot --log-json execution.jsonl "your goal here"

# Example
nitropilot --log-json deploy.jsonl \
 "Install nginx, configure it for my React app, and start it"
```

### Advanced Options

```bash
# Limit execution steps
nitropilot --log-json run.jsonl --max-steps 50 "complex task"

# Output only final results to stdout
nitropilot --log-json run.jsonl --stdout-results "task"

# Replay a previous execution (deterministic, no API calls)
nitropilot --replay-json previous-run.jsonl
```


## 📖 Documentation

### Architecture

```
┌─────────────┐
│   User      │
│   Prompt    │
└──────┬──────┘
      │
      ▼
┌─────────────────────────┐
│   High-Level Planner    │
│  (Claude Sonnet 4-5)    │
└──────────┬──────────────┘
          │
          ▼
┌──────────────────────────┐
│   Execution Engine       │
│ • Environment gathering  │
│ • Command execution      │
│ • Validation loop        │
│ • Auto-remediation       │
└──────────┬───────────────┘
          │
          ▼
┌──────────────────────────┐
│   Structured Logs        │
│ (JSONL audit trail)      │
└──────────────────────────┘
```

### How It Works

1. **Planning**: NitroPilot analyzes your goal and creates a high-level execution plan
2. **Context Gathering**: Collects relevant environment information (OS, installed tools, file structure)
3. **Step Execution**: Runs commands incrementally, validating each step
4. **Self-Correction**: If a step fails, automatically diagnoses and remediates
5. **Completion**: Verifies success criteria and provides detailed summary

### Log Format

Every execution produces a JSONL log file:

```jsonl
{"ts_unix":1704067200,"kind":"event","event":"run_start","prompt":"deploy app"}
{"ts_unix":1704067201,"kind":"event","event":"plan","plan":{"summary":"..."}}
{"ts_unix":1704067202,"kind":"event","event":"next_step","step":{"title":"..."}}
{"ts_unix":1704067203,"kind":"event","event":"exec_result","stdout":"...","rc":0}
{"ts_unix":1704067204,"kind":"event","event":"validation","validation":{"ok":true}}
```

Perfect for:


## 🎯 Use Cases

### Power Users

### DevOps Automation

### Development Workflows

### System Administration

### Data Engineering


## 🤝 Contributing

We welcome contributions! Here's how to help:

### Ways to Contribute

1. **⭐ Star the repo** - Help us reach 20K!
2. **🐛 Report bugs** - [Open an issue](https://github.com/tonivega/nitropilot/issues)
3. **💡 Suggest features** - [Start a discussion](https://github.com/tonivega/nitropilot/discussions)
4. **📖 Improve docs** - Submit a PR


## 🌟 Why NitroPilot Will Change Everything

### The Future of Development

We believe the next 10 years of software development will be characterized by:

1. **Natural Language as the Primary Interface**: Developers will describe *what* they want, not *how* to do it
2. **Autonomous Execution**: AI agents that don't just suggest, but act
3. **Self-Healing Systems**: Software that detects and fixes its own issues
4. **Democratized Expertise**: Junior developers with senior-level productivity

**NitroPilot is the first step toward this future.**

### Community-Driven Innovation

At 20,000 stars, we'll open source:

**Your star isn't just support—it's an investment in the future of autonomous software.**


## 📊 Metrics & Benchmarks

### Cost

Usually, lower token usage than alternatives.

### Performance

Usually, not slower than alternatives.

## 🔒 Security

NONE (can access anything in your device and at this moment no efforts has been made to be prompt injection resistant)

No telemetry is included in the executable.

## 📜 License

No Warranty/Liability: The software is provided "as is," without any guarantees, and authors aren't liable for damage

**Current Release**: Shareware - Proprietary Software

**After 20K Stars**: MIT License - use it anywhere, commercially or personally


## 🙏 Acknowledgments

Special thanks to early adopters and contributors!

[sergiopr89](https://github.com/sergiopr89) for seeding the idea with his project [TalosBot](https://github.com/talosbotoss/talosbot) 

## 💬 Community



<div align="center">

## ⭐ Star Us to Unlock Full Source! ⭐

**20,000 stars = Complete MIT-licensed codebase**

[![Star on GitHub](https://img.shields.io/github/stars/tonivega/nitropilot?style=social)](https://github.com/tonivega/nitropilot)

### 🚀 **[Star Now →](https://github.com/tonivega/nitropilot)**


Made with ❤️ by the NitroPilot team

[Website](https://wwww.nitrobutton.com) • [Blog](https://www.kardanow.com) • [Mothership](https://www.bluengo.com)

</div>
