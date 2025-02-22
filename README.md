# AutoAI-Starter 🚀  

_A self-hosted AI automation framework, built on Self-hosted AI Starter Kit by the n8n team and enhanced with Cloudflare, Chat GUI, Database, and RAG. Forked from @tuyenhm68._

AutoAI is a powerful toolkit designed to simplify the deployment and operation of autonomous AI Agents, leveraging the capabilities of n8n and self-hosted AI technologies. The toolkit integrates essential components such as Local AI, Open WebUI, Flowise, and more to support comprehensive AI workflows.

## 🌟 Features  
- **Cloudflare Integration**: Secure domain & performance optimization  
- **Chat GUI**: Interactive AI-powered conversations  
- **Database Support**: Persistent storage for workflows  
- **RAG (Retrieval-Augmented Generation)**: Smarter AI with knowledge retrieval  

## 🧪 Installation  
1. Clone this repo:  
   ```bash
   git clone https://github.com/kientranasia/AutoAI-Starter.git
   cd AutoAI-Starter
   ```
---

# Self-hosted AI Starter Kit (by the n8n team)

**Self-hosted AI Starter Kit** is an open-source Docker Compose template that quickly bootstraps a fully featured Local AI and Low Code development environment, including Open WebUI for interacting with your n8n agents.

This version includes improvements and additional features such as Open WebUI and Flowise. The local RAG AI Agent workflow from the demo video will be automatically included in your n8n instance using this setup.

[Original Local AI Starter Kit](https://github.com/n8n-io/self-hosted-ai-starter-kit)

## 🚀 Quick Start

### For Nvidia GPU users
```bash
git clone https://github.com/kientranasia/AutoAI-Starter.git
cd AutoAI-Starter
docker compose --profile gpu-nvidia up
```

> **Note:** If using an Nvidia GPU with Docker for the first time, follow the [Ollama Docker instructions](https://github.com/ollama/ollama/blob/main/docs/docker.md).

### For Mac / Apple Silicon users
```bash
git clone https://github.com/kientranasia/AutoAI-Starter.git
cd AutoAI-Starter
docker compose up
```

If running Ollama on Mac, set credentials to `http://host.docker.internal:11434/`.

### For CPU-only users
```bash
git clone https://github.com/kientranasia/AutoAI-Starter.git
cd AutoAI-Starter
docker compose --profile cpu up
```

## 🔋 Running AI Agents
1. Open **n8n** at [http://localhost:5678/](http://localhost:5678/) and complete the initial setup.
2. Open the workflow at [http://localhost:5678/workflow/vTN9y2dLXqTiDfPT](http://localhost:5678/workflow/vTN9y2dLXqTiDfPT).
3. Set up credentials for:
   - **Ollama**: `http://ollama:11434`
   - **PostgreSQL**: Use credentials from `.env` file.
   - **Qdrant**: `http://qdrant:6333`
   - **Google Drive**: Follow [this guide](https://docs.n8n.io/integrations/builtin/credentials/google/).
4. Toggle the workflow **Active** and copy the "Production" webhook URL.
5. Open **Open WebUI** at [http://localhost:3000/](http://localhost:3000/), go to Workspace -> Functions, and add a function using `n8n_pipe.py`.
6. Configure `n8n_url` with the copied webhook URL.

## 🚀 Upgrading

### For Nvidia GPU users
```bash
docker compose --profile gpu-nvidia pull
docker compose create && docker compose --profile gpu-nvidia up
```

### For Mac / Apple Silicon users
```bash
docker compose pull
docker compose create && docker compose up
```

### For CPU-only users
```bash
docker compose --profile cpu pull
docker compose create && docker compose --profile cpu up
```

## 💡 Additional Resources
- [AI Agents for Developers](https://blog.n8n.io/ai-agents/)
- [Build an AI Workflow in n8n](https://docs.n8n.io/advanced-ai/intro-tutorial/)
- [Langchain in n8n](https://docs.n8n.io/advanced-ai/langchain/langchain-n8n/)
- [Video Guide](https://youtu.be/V_0dNE-H2gw)
- [AI Templates Gallery](https://n8n.io/workflows/?categories=AI)

## © Copyright
Forked from @tuyenhm68. Based on the **Self-hosted AI Starter Kit** by n8n. All rights reserved to the respective owners.
