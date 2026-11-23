# UseAgent Free — সেটআপ (বাংলা)

Source: https://github.com/useagenthq/useagent

## চালানোর উপায়
```
git clone https://github.com/useagenthq/useagent.git
cd useagent
# এই repo-র docker-compose.yml ফাইলটি এখানে (repo root-এ) রাখুন
docker compose up -d --build
```
তারপর http://localhost:3400 খুলুন (backend :3201)।

## আগের ভুলটা কী ছিল
আগের compose ফাইলে `useagent/backend:latest` আর `useagent/frontend:latest` ইমেজ ব্যবহার করা হয়েছিল — ওই নামে কোনো পাবলিশড ইমেজ নেই, তাই `docker compose up` পুল করতে গিয়ে ফেল করতো। এখন Dockerfile.backend / Dockerfile.frontend দিয়ে সোর্স থেকে বিল্ড হয়।

## কী লাগবে
- Docker + Docker Compose
- Postgres 16 (pgvector) — compose ফাইলে দেওয়া আছে
- একটি মডেল কী (Groq / OpenRouter / Gemini ফ্রি কী) — অথবা Ollama লোকাল মডেল

## ফ্রি পথ
Ollama চালিয়ে `OLLAMA_URL=http://host.docker.internal:11434` সেট করুন, তাহলে কোনো পেইড কী ছাড়াই চলবে।
