# AutoAI-Starter 🚀

_AutoAI-Starter is a self-hosted AI automation framework, customized and maintained by **Athsent** for the **AutoAI** product line._

## About AutoAI-Starter

AutoAI-Starter provides a robust, extensible platform for deploying and operating autonomous AI agents. Built on the foundation of the n8n team's Self-hosted AI Starter Kit, this version is enhanced and maintained by Athsent, with additional integrations and optimizations for enterprise and product use.

**Key Features:**
- **Cloudflare Integration:** Secure, performant domain management
- **Chat GUI:** Interactive, AI-powered conversations
- **Database Support:** Persistent workflow storage
- **RAG (Retrieval-Augmented Generation):** Smarter AI with knowledge retrieval
- **Local LLMs:** Run advanced language models on your own hardware

---

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/kientranasia/AutoAI-Starter.git
cd AutoAI-Starter
```

### 2. Start the Stack

- **For Nvidia GPU:**
  ```bash
  docker compose --profile gpu-nvidia up
  ```
- **For Mac/Apple Silicon or CPU-only:**
  ```bash
  docker compose --profile cpu up
  ```

> **Note:** Ensure Docker is running on your system before starting.

---

## 🛠️ Components

- **n8n:** Low-code automation platform (http://localhost:5678/)
- **Ollama:** Local LLM server (http://localhost:11434/)
- **Qdrant:** Vector database (http://localhost:6333/)
- **PostgreSQL:** Relational database

---

## 🧑‍💻 Usage

1. Access n8n at [http://localhost:5678/](http://localhost:5678/) and complete the initial setup.
2. Configure credentials for Ollama, Postgres, and Qdrant as needed.
3. Import or create your AI workflows in n8n.
4. Use the provided workflow templates or build your own automations.
5. Monitor logs and service health via Docker.

---

## 🏢 About Athsent

This repository is maintained and customized by **Athsent** as part of the **AutoAI** product suite. For enterprise support, custom integrations, or product inquiries, please contact us at [info@athsent.com](mailto:info@athsent.com).

---

## 📚 Resources

- [n8n Documentation](https://docs.n8n.io/)
- [Ollama Documentation](https://ollama.com/)
- [Qdrant Documentation](https://qdrant.tech/)
- [PostgreSQL Documentation](https://www.postgresql.org/)

---

## 📝 License

This project is licensed under the MIT License.
