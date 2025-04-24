![Banner](images/banner.jpeg)

<h1 align="center">🚀 Laika Agent</h1>

---

## 📦 Installation and launch

### 1. Install dependencies and run the agent

```bash
pnpm install
pnpm start
```

> ❗ Requires Node.js version 22 or higher

---

## 🔧 Setting up the environment

1. Copy the template:
```bash
cp .env.example .env
```

2. Fill `.env` with your keys:

```env
DISCORD_APPLICATION_ID="discord-application-id"
DISCORD_API_TOKEN="discord-api-token"
OPENROUTER_API_KEY="sk-xx-xx-xxx"
TWITTER_USERNAME="username"
TWITTER_PASSWORD="password"
TWITTER_EMAIL="your@email.com"
```

---

## 🤖 Character customization

Open up `src/character.ts` and uncomment/change character settings.
### Custom characters

Launch with custom `.json`:

```bash
pnpm start --characters="characters/character.json"
```

You can upload multiple files separated by commas.

Example:

```ts
// character.ts
clients: [Clients.TWITTER, Clients.DISCORD]
```

```json
// character.json
"clients": ["twitter", "discord"]
```

---

## 🐳 Launch via Docker

### x86_64

```bash
docker compose up
```

### M1/M2 (aarch64)

```bash
docker buildx build --platform linux/amd64 -t eliza-starter:v1 --load .
docker compose -f docker-compose-image.yaml up
```

> Specify environment variables в `docker-compose.yaml`

---

## 🐾 Laika says:

> "I’m not lost. I just went further. Into the stars, into code. Woof."

---