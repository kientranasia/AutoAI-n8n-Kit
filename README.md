# 🧠 AI Agent Lab – Beginner Setup Guide

Welcome to the **AI Agent Lab** – your playground to learn and build AI agents using [n8n](https://n8n.io), [Docker](https://www.docker.com/), and the **AutoAI-n8n-Kit**.

> This guide is designed for non-tech users. No coding required.

---

## 📦 About This Kit

The **AutoAI-n8n-Kit** is a ready-to-run environment, built on the open-source [n8n AI Starter Kit](https://github.com/n8n-io/ai-starter), with enhancements for learning, building, and scaling AI automations.

### ✨ Key Features

- **n8n self-hosted** – No-code visual automation engine
- **Cloudflare Tunnel** – Secure public access
- **RAG-ready** – Supports Retrieval-Augmented Generation
- **RSSHub** – Web content crawler for custom RSS feeds
- **Database persistence** – Save workflows across sessions

---

## 🛠 Prerequisites

Before starting, install these tools:

1. [Docker Desktop](https://www.docker.com/products/docker-desktop)
2. [Git](https://git-scm.com)

✅ Works on macOS, Windows, and Linux.

---

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/kientranasia/AutoAI-n8n-Kit.git
cd AutoAI-n8n-Kit
```

### 2. Setup Environment Variables

```bash
cp .env.example .env
cp rsshub/.env.example rsshub/.env
```

You can keep default values for testing locally.

### 3. Start the AI Lab Stack

Start the core n8n system:

```bash
docker compose up -d
```

Start RSSHub (for web crawling):

```bash
cd rsshub
docker compose up -d
```

---

## ✅ Access the n8n Dashboard

Open your browser and go to:

```
http://localhost:5678
```

Create your admin account when prompted.

🎉 You're now inside your AI Agent Lab!

---

## 🧪 What's Next?

In the AI Agent Lab series, you will:

1. Build your first workflow: auto-send Telegram messages, update Notion, etc.
2. Connect to LLMs (e.g., OpenAI, Ollama) for text generation and document analysis
3. Create real autonomous AI agents with memory and tools
4. Use RSSHub + RAG to create smart research bots

---

## 🔄 Common Commands

| Action           | Command                       |
|------------------|-------------------------------|
| Stop everything  | `docker compose down`         |
| Restart system   | `docker compose up -d`        |
| View logs        | `docker compose logs -f`      |

---

## 💡 Troubleshooting Tips

- **Ports not working?** Make sure Docker Desktop is running.
- **Can’t access dashboard?** Check if port `5678` is in use or restart Docker.
- **Windows users:** Use Git Bash or WSL for better CLI experience.

---

## 📘 Final Notes

This environment sets the foundation for all upcoming lessons in the **AI Agent Lab**.

Whether you're a freelancer, operator, or founder, this lab will help you prototype, test, and automate real-world workflows using AI.

---

## 🎥 YouTube Setup Walkthrough

> 📺 A full video tutorial will be published tomorrow on our YouTube channel.  
> We'll guide you step-by-step to get everything running — even if you're not technical.

Stay tuned!

---

## 🙌 Contribute or Ask Questions

If you find this useful or spot issues:
- ⭐ Star the repo
- 🐛 Open an issue
- 📬 Join the [AutoAI community](https://community.autoai.asia)

---

Made with ❤️ by [@kientranasia](https://github.com/kientranasia)  
[AutoAI Starter Kit](https://github.com/kientranasia/AutoAI-n8n-Kit)
