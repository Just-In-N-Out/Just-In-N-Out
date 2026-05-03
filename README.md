<h1 align="center">Justin Issa</h1>
<h3 align="center">Software Engineer | Aspiring AppSec & DevSecOps Engineer</h3>

---

## About Me

I'm a full-stack software engineer who thinks like a security engineer. I build production systems end-to-end — backends, real-time pipelines, mobile apps — and design them with secure architecture from day one rather than bolting it on later.

Graduating from Arizona State University in May 2026 and starting my Master's in Cybersecurity at Georgia Tech (Information Security track) in Fall 2026. My focus:

- Full-stack engineering — distributed systems, async pipelines, real-time WebSocket platforms
- DevSecOps — embedding SAST, SCA, container scanning, and SARIF-driven merge gates into CI/CD
- Application security — threat modeling, secure-by-default architecture, AI/LLM hardening

---

## Featured Projects

### 3DSearch — Real-Time 3D Model Aggregation Platform
`Python` `Django` `React` `PostgreSQL` `Celery` `Redis` `Docker` `GitHub Actions`

> Software Engineering Internship at [LinkClicks](https://linkclicks.io) — [3dsearch.org](https://3dsearch.org/)

- Django 5 + DRF backend with 13 REST endpoints, 10 PostgreSQL models, and ~350 pytest tests, deployed via Docker Compose (7 services) to AWS EC2 with multi-architecture (amd64 + arm64) container builds
- Async ingestion pipeline on Celery + Redis aggregating 5 third-party APIs over HTTP/2, sustaining ~240 models ingested per day with zero rate-limit bans across platforms
- Real-time streaming search via Django Channels and Redis pub/sub, replacing client polling with WebSocket push updates
- 3-layer prompt injection defense modeled on OWASP LLM01 (sanitization, label wrapping, output validation) blocking adversarial misuse of integrated AI features
- Trivy-based GitHub Actions DevSecOps pipeline gated on HIGH/CRITICAL findings — caught 3 real CVEs pre-merge over the project's lifetime

### [LLM Vulnerability Scanner](https://github.com/Just-In-N-Out/LLM-Vulnerability-Scanner) — Reusable DevSecOps Pipeline for AI Apps
`Python` `GitHub Actions` `SARIF` `Pydantic` `OWASP LLM Top 10`

- Reusable GitHub Actions workflow (`workflow_call`, 305 LOC) chaining 4 SAST and dependency scanners (custom LLM scanner, Bandit, Semgrep, pip-audit) in a parallel matrix, each emitting SARIF 2.1.0 to the GitHub Security tab
- Typed Pydantic SARIF emitter and cross-tool severity aggregator driving a configurable merge gate that blocks pull requests when findings exceed a threshold
- Edit-in-place PR comment job summarizing findings across tools, backed by 70 passing tests covering the SARIF schema, gate logic, and rule-engine outputs

### [MinimaLog](https://github.com/Just-In-N-Out/MinimaLog) — iOS Workout Tracking App
`TypeScript` `React` `Supabase` `PostgreSQL` `Capacitor` — [minimalog.fit](https://minimalog.fit)

- Normalized PostgreSQL schema (20 tables) with 100 row-level security policies enforcing per-user authorization at the database layer, eliminating IDOR risk
- Offline-first sync engine buffering writes to IndexedDB during network loss, replaying them to PostgreSQL on reconnect, and resolving temporary client IDs to UUIDs
- OAuth 2.0 PKCE flows with redirect URI allowlist blocking open-redirect attacks during native deep-link callbacks across two identity providers
- AES-256-GCM encryption (PBKDF2-derived keys, 100,000 iterations) for session tokens and sensitive local storage, with HMAC-SHA256-verified third-party webhooks
- Shipped to the iOS App Store and minimalog.fit with optimistic UI updates and 400ms-debounced writes that decouple user input from network round-trips

---

## Tech Stack

<div align="center">

**Languages & Frameworks**

<img src="https://skillicons.dev/icons?i=python,ts,js,react,nodejs,django,postgres,redis" />

**Cloud & DevOps**

<img src="https://skillicons.dev/icons?i=docker,aws,linux,bash,nginx,githubactions,vercel" />

</div>

<div align="center">
  <img src="https://img.shields.io/badge/Burp_Suite-FF6633?style=for-the-badge&logo=burp-suite&logoColor=white" />
  <img src="https://img.shields.io/badge/Trivy-1904DA?style=for-the-badge&logo=trivy&logoColor=white" />
  <img src="https://img.shields.io/badge/Semgrep-1B2B34?style=for-the-badge&logo=semgrep&logoColor=white" />
  <img src="https://img.shields.io/badge/Bandit-FFD400?style=for-the-badge&logoColor=black" />
  <img src="https://img.shields.io/badge/SARIF-1F2328?style=for-the-badge&logoColor=white" />
  <img src="https://img.shields.io/badge/OWASP-000000?style=for-the-badge&logo=owasp&logoColor=white" />
</div>

---

## My Contributions

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Just-In-N-Out/Just-In-N-Out/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Just-In-N-Out/Just-In-N-Out/output/github-contribution-grid-snake.svg" />
    <img alt="github-snake" src="https://raw.githubusercontent.com/Just-In-N-Out/Just-In-N-Out/output/github-contribution-grid-snake-dark.svg" />
  </picture>
</div>
