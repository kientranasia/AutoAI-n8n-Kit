# AutoAI-Starter-Kit 🚀

_AutoAI-Starter-Kit is a self-hosted AI automation framework, customized and maintained by **Athsent** for the **AutoAI** product line._

![n8n Demo Flow](assets/n8n-demo.gif)

*Visual demo: Example n8n workflow in action.*

---

## About AutoAI-Starter-Kit

AutoAI-Starter-Kit provides a robust, extensible platform for deploying and operating autonomous AI agents. It is built on the n8n team's Self-hosted AI Starter Kit and enhanced by Athsent for enterprise and product use.

**Key Features:**
- **Cloudflare Integration:** Secure, performant domain management
- **Database Support:** Persistent workflow storage
- **RAG (Retrieval-Augmented Generation):** Smarter AI with knowledge retrieval
- **Custom RSS Feeds:** Self-hosted RSSHub for crawling and generating feeds from any website

---

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/kientranasia/AutoAI-n8n-Kit.git
cd AutoAI-n8n-Kit
```

### 2. Configure Environment Variables

- Copy `.env.example` to `.env` in the root and in `rsshub/`:
  ```bash
  cp .env.example .env
  cp rsshub/.env.example rsshub/.env
  ```
- Edit the `.env` files to set your secrets and credentials.

### 3. Start the Main Stack

```bash
docker compose up -d
```

### 4. Start RSSHub

```bash
cd rsshub
docker compose up -d
```

---

## 🛠️ Components

- **n8n** (`autoai-n8n`): Low-code automation platform ([http://localhost:5678/](http://localhost:5678/))
- **Qdrant** (`autoai-qdrant`): Vector database ([http://localhost:6333/](http://localhost:6333/))
- **PostgreSQL** (`autoai-postgres`): Relational database
- **Cloudflare Tunnel** (`autoai-cloudflare-tunnel`): Secure remote access
- **RSSHub** (`autoai-rsshub`): Self-hosted RSS feed generator ([http://localhost:1200/](http://localhost:1200/))

---

## 🧑‍💻 Usage

1. Access n8n at [http://localhost:5678/](http://localhost:5678/) and complete the initial setup.
2. Configure credentials for Postgres and Qdrant as needed.
3. Import or create your AI workflows in n8n.
4. Use RSSHub to generate custom RSS feeds from any website.  
   - If you enabled Basic Auth, use the credentials from `rsshub/.env` (`AUTH_USER`/`AUTH_PASS`).
   - Example API call:  
     ```
     curl -u autoai:changeme123 http://localhost:1200/github/trending/daily
     ```
5. Integrate RSSHub feeds into n8n using the HTTP Request node with Basic Auth.
6. Monitor logs and service health via Docker.

---

## 🏢 About Athsent

This repository is maintained and customized by **Athsent** as part of the **AutoAI** product suite. For enterprise support, custom integrations, or product inquiries, please contact us at [info@athsent.com](mailto:info@athsent.com).

---

## 📚 Resources

- [n8n Documentation](https://docs.n8n.io/)
- [Qdrant Documentation](https://qdrant.tech/)
- [PostgreSQL Documentation](https://www.postgresql.org/)
- [Cloudflare Tunnel Documentation](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/)
- [RSSHub Documentation](https://docs.rsshub.app/)

---

## 📝 License

This project is licensed under the MIT License.
