# 🌸 Hi, I'm Lumi

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=24&duration=3000&pause=1000&color=F5C6D0&center=true&vCenter=true&width=850&lines=Computer+Engineering+%7C+Cloud+%7C+Network+%7C+Backend;Building+systems%2C+not+just+interfaces.;ACG+%C3%97+Cloud+Infrastructure+%C3%97+AI+%C3%97+Security" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://github.com/Lumichandesu">
    <img src="https://img.shields.io/badge/GitHub-Lumichandesu-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://www.linkedin.com/in/lumichandesu/">
    <img src="https://img.shields.io/badge/LinkedIn-Lumichandesu-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="https://yomumi.moe">
    <img src="https://img.shields.io/badge/Yomumi-yomumi.moe-F5C6D0?style=for-the-badge&logo=cloudflare&logoColor=333333" />
  </a>
</p>

<p align="center">
  <b>Computer Engineering · Network Engineering · Cloud Infrastructure · Backend Systems · AI-assisted Development</b>
</p>

---

## 👋 About Me

I'm **Lumi (Lumichandesu)**, a Computer Engineering graduate who enjoys building complete systems rather than isolated demos.

My interests sit at the intersection of:

* 🌐 Network Engineering
* ☁️ Cloud Infrastructure
* ⚡ High-performance Backend Systems
* 🗄️ Distributed Databases & Caching
* 🔐 Application & Infrastructure Security
* 🤖 AI-assisted Software Engineering
* 🎨 Creative Technology & ACG platforms

I especially enjoy working on problems involving **latency, resource efficiency, scalability, reliability, security boundaries, and real-world deployment**.

> I don't just ask whether a system works.
> I care about **how fast it is, how much it costs, how it scales, how it fails, and how securely it recovers**.

---

# 🚀 Featured Project

## 🌸 Yomumi — よむみ

> **Every Story Begins with a Dream.**

**Yomumi** is my main long-term project: a next-generation ACG publishing and creative ecosystem focused on web novels, vertical webtoons, anime tracking, creator tools, community systems, AI-assisted workflows, and creator monetization.

🌐 **Production:** https://yomumi.moe

### Architecture

```text
                           ┌───────────────────────────────┐
                           │          USER BROWSER         │
                           │  Astro SSR / Reader / PWA    │
                           └───────────────┬───────────────┘
                                           │
                                  HTTPS / Edge Delivery
                                           │
                                           ▼
                    ┌─────────────────────────────────────────┐
                    │          CLOUDFLARE EDGE                │
                    │                                         │
                    │  Workers · DNS · Global Edge · R2      │
                    └───────────────┬─────────────────────────┘
                                    │
                              HTTPS / API
                                    │
                                    ▼
                    ┌─────────────────────────────────────────┐
                    │       GOOGLE CLOUD RUN                  │
                    │       asia-southeast1                  │
                    │                                         │
                    │   Bun · ElysiaJS · REST API             │
                    │   Authentication · Security            │
                    │   Monetization · Creator Services      │
                    └───────┬──────────────┬──────────────────┘
                            │              │
               ┌────────────┘              └─────────────┐
               ▼                                         ▼
     ┌───────────────────┐                  ┌────────────────────┐
     │ Neon PostgreSQL   │                  │   Upstash Redis    │
     │ AWS Singapore     │                  │   Tokyo / Japan    │
     │ ACID + Drizzle    │                  │ Rate Limit / Cache │
     └─────────┬─────────┘                  └────────────────────┘
               │
               ▼
     ┌────────────────────┐
     │ Financial Ledger   │
     │ OAuth · AI · R2    │
     │ Stripe · PromptPay │
     └────────────────────┘
```

### Core Engineering Goals

* ⚡ Low-latency request processing
* 🌍 Edge-first frontend delivery
* 🧩 Multi-instance-safe backend architecture
* 🔐 Server-authoritative authentication and authorization
* 🪙 Atomic financial ledger operations
* 🚦 Distributed Redis rate limiting
* 🗄️ PostgreSQL as the persistent source of truth
* 🤖 Gemini-powered creator tooling
* 📦 Cloud object storage with scoped presigned URLs
* 🛡️ Security-first API boundaries

### Current Core Stack

| Layer              | Technology                    |
| ------------------ | ----------------------------- |
| Frontend           | Astro                         |
| Styling            | Tailwind CSS                  |
| Runtime            | Bun                           |
| API                | ElysiaJS                      |
| Database           | PostgreSQL                    |
| ORM                | Drizzle ORM                   |
| Cache / Rate Limit | Redis / Upstash               |
| Cloud              | Google Cloud Run              |
| Edge               | Cloudflare Workers            |
| Storage            | Cloudflare R2                 |
| Authentication     | JWT + Argon2id + Arctic OAuth |
| AI                 | Google Gemini                 |
| Payments           | Stripe + PromptPay            |

🔗 **Project:** https://github.com/Lumichandesu/subculture-platform
🌐 **Website:** https://yomumi.moe

---

# 🧩 Other Projects

## 🎙️ VTuber Real-Time OBS AI Subtitle & Live Translator

A standalone real-time subtitle and live translation tool designed for VTubers and streamers.

The project focuses heavily on **latency-sensitive local processing, OBS integration, subtitle rendering, localization, and lightweight execution**.

### Highlights

* ⚡ Ultra-low-latency subtitle pipeline
* 🎙️ Dual-worker speech recognition architecture
* 🌸 Thai / Japanese / English support
* 📺 Transparent OBS Browser Source overlay
* 🛡️ Localhost-only security boundary
* 🎨 Anime-focused typography and subtitle styling
* 🔄 Continuous speech processing
* 🧠 AI-assisted translation workflows

### Technology

```text
Bun
├── React 19
├── Speech / STT pipeline
├── Translation pipeline
├── OBS Browser Source
└── Localhost service
```

🔗 https://github.com/Lumichandesu/vtuber-subtitle-studio

The repository documents a real-time subtitle/translation workflow targeting sub-40ms translation latency and a lightweight local architecture.

---

## 🎵 Lumi Discord Bot

A lightweight Discord music bot designed around **low resource consumption and long-running uptime**.

One of the primary engineering goals was reducing unnecessary infrastructure overhead by eliminating an external Lavalink dependency and moving to a native voice/audio pipeline.

### Highlights

* ⚡ Bun-based runtime
* 🎧 Native Discord voice streaming
* 🪶 Lightweight memory footprint
* 🔎 Multi-platform media metadata resolution
* 🎼 Lyrics integration
* 🎛️ Interactive Discord controls
* 📊 Runtime telemetry
* 🚪 Automatic idle disconnect
* ⌨️ Command aliases

### Engineering Focus

```text
Discord
   │
   ▼
Discord.js
   │
   ├── Voice Gateway
   ├── Command System
   ├── Queue Manager
   └── Telemetry
          │
          ▼
      Native Audio
      + FFmpeg
```

The repository describes the native engine as a replacement for external Lavalink nodes, with a target footprint below roughly 80 MB versus a much heavier Lavalink-based setup.

🔗 https://github.com/Lumichandesu/lumi-discord-bot

---

## ⚡ Bun + Elysia Fast Starter

A production-oriented backend starter focused on **speed, low resource consumption, API design, authentication, observability, WebSockets, and modern TypeScript infrastructure**.

### Highlights

* ⚡ Bun runtime
* 🛠️ Type-safe ElysiaJS API
* 🗄️ Drizzle ORM
* 🔐 JWT + Argon2id
* 🔄 WebSocket support
* 🚦 Rate limiting
* 📊 Runtime telemetry
* 📁 Upload APIs
* 🧪 Automated test suite
* 🐳 Docker deployment
* 🤖 GitHub Actions CI

### Architecture

```text
Client
  │
  ▼
Elysia API
  │
  ├── Auth
  │    └── JWT / Argon2id
  │
  ├── Tasks
  │    └── CRUD / WebSocket
  │
  ├── Upload
  │
  ├── Health
  │    └── Runtime metrics
  │
  └── Database
       └── Drizzle ORM
```

The project README positions it as a minimalist production-ready REST/SaaS starter and includes CI, Docker, WebSockets, telemetry, authentication, uploads, and automated testing.

🔗 https://github.com/Lumichandesu/elysia-fast-starter

---

# 🛠️ Technical Interests

### Backend & Systems

```text
TypeScript
Bun
ElysiaJS
REST APIs
WebSockets
Server-Sent Events
Distributed Systems
Concurrency
Caching
Queues
Observability
```

### Cloud & Infrastructure

```text
Google Cloud
Cloud Run
Cloudflare
Workers
R2
DNS
Serverless Infrastructure
Containerization
CI/CD
```

### Databases

```text
PostgreSQL
Neon
Drizzle ORM
Redis
Upstash
Database Transactions
ACID
Idempotency
Query Optimization
```

### Security

```text
JWT
OAuth 2.0
Argon2id
RBAC
CORS
Rate Limiting
IDOR Prevention
CSRF Protection
Input Validation
Security Headers
Fail-Closed Design
```

### AI

```text
Google Gemini
AI-assisted Development
Prompt Engineering
AI Security
Lore / Context Analysis
Translation
Proofreading
Creator Copilot Workflows
```

### Networking

```text
Cisco
VLAN
Inter-VLAN Routing
NAT / PAT
DHCP
DNS
QoS
Firewalls
Routing
Network Monitoring
Infrastructure Troubleshooting
```

---

# 🧠 Engineering Philosophy

```text
Performance
    ↓
Measure before optimizing
    ↓
Optimize critical paths
    ↓
Minimize unnecessary work
    ↓
Validate with real telemetry
    ↓
Design for failure
    ↓
Secure every trust boundary
    ↓
Scale only after the architecture is correct
```

I prefer systems where:

* the database is the authority for persistent state,
* the application does not trust client-controlled identity,
* financial operations are atomic,
* retries are idempotent,
* distributed instances share security state,
* failures are explicit instead of silently corrupting state,
* performance is measured rather than guessed.

---

# 📊 GitHub & Activity

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Lumichandesu&show_icons=true&hide_border=true&rank_icon=github" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Lumichandesu&layout=compact&hide_border=true" alt="Top Languages" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=Lumichandesu&hide_border=true" alt="GitHub Streak" />
</p>

---

# 📈 What I'm Building

### Current Focus

* 🌸 **Yomumi**
* ☁️ Cloud infrastructure
* 🔐 Application security hardening
* ⚡ Performance and latency optimization
* 📊 Production telemetry and observability
* 🤖 AI-assisted creator workflows
* 🧩 Distributed application architecture

### Long-Term Direction

```text
Network Engineering
        +
Cloud Infrastructure
        +
Backend Engineering
        +
AI Systems
        +
Security
        +
Creative Technology
        ↓
      YOMUMI
```

---

# 🌐 Links

| Platform                  | Link                                                   |
| ------------------------- | ------------------------------------------------------ |
| GitHub                    | https://github.com/Lumichandesu                        |
| LinkedIn                  | https://www.linkedin.com/in/lumichandesu/              |
| Yomumi                    | https://yomumi.moe                                     |
| Yomumi Source             | https://github.com/Lumichandesu/subculture-platform    |
| VTuber Subtitle Studio    | https://github.com/Lumichandesu/vtuber-subtitle-studio |
| Lumi Discord Bot          | https://github.com/Lumichandesu/lumi-discord-bot       |
| Bun + Elysia Fast Starter | https://github.com/Lumichandesu/elysia-fast-starter    |

---

# 🌸 A Little More About Me

```text
I like networks.
I like clouds.
I like fast systems.
I like clean architecture.
I like anime.
I like building things.

So I combined them.
```

> **Every Story Begins with a Dream.**
> **すべての物語は、ひとつの夢から始まる。**

---

<p align="center">
  <sub>Built with curiosity, caffeine, and an unreasonable amount of debugging.</sub>
</p>

<p align="center">
  <b>© 2026 Lumichandesu</b>
</p>
