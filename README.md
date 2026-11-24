# 🤖 useagent-free

[![AI Agent](https://img.shields.io/badge/type-ai%20coding%20agent-blue)](https://github.com/tunnabri-ops/useagent-free)
[![Language](https://img.shields.io/badge/UI-Bangla%20%2B%20English-orange)](https://github.com/tunnabri-ops/useagent-free)

**Free self-hosted AI coding agent — builds from source with one docker compose command, with a local-model path via Ollama.**

> বাংলা সংস্করণ নিচে আছে। / Bangla version below.

## ✨ Features

- **Builds from source** — the compose file builds the backend and frontend from `Dockerfile.backend` / `Dockerfile.frontend`, because no published images exist for them
- **Postgres 16 with pgvector** included in the compose file
- **Backend on `:3201`, UI on `:3400`** — the frontend proxies `/api/*` to the backend
- **Free path** — run Ollama and set `OLLAMA_URL=http://host.docker.internal:11434` to work with no paid key

## 🚀 How to use

```bash
# Place docker-compose.yml in the repo root, then:
docker compose up -d --build
```

Then open http://localhost:3400 (backend on :3201).

## ⚠️ Honest limits

- Needs Docker + Docker Compose.
- You need a model key (Groq / OpenRouter / Gemini free key) **or** a local Ollama model.
- A sandbox provider key is still needed per the setup, even on the free path.

## 🇧🇩 বাংলা

**ইউজএজেন্ট ফ্রি — নিজের সার্ভারে ফ্রি AI কোডিং এজেন্ট।**

- `docker-compose.yml` রেপো রুটে রেখে `docker compose up -d --build` চালান
- তারপর http://localhost:3400 খুলুন (ব্যাকএন্ড :3201)
- পেইড কী ছাড়া চালাতে Ollama চালিয়ে `OLLAMA_URL` সেট করুন

## 📄 License

MIT — use it however you like; credit is appreciated.
