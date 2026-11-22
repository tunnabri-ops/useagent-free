# UseAgent Free — সেটআপ (বাংলা)

Source: https://github.com/useagenthq/useagent

## এক কমান্ডে চালান
```
docker compose up -d
```
তারপর http://localhost:3000 খুলুন।

## কী লাগবে
- Docker + Docker Compose
- Postgres 16 (pgvector) — compose ফাইলে দেওয়া আছে
- একটি মডেল কী (Groq / OpenRouter / Gemini ফ্রি কী) — অথবা Ollama লোকাল মডেল

## ফ্রি পথ
Ollama চালিয়ে `OLLAMA_URL=http://host.docker.internal:11434` সেট করুন, তাহলে কোনো পেইড কী ছাড়াই চলবে।
