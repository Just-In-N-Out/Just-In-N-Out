<h1 align="center">Justin Issa</h1>
<h3 align="center">Software Engineer | AppSec & DevSecOps Engineer</h3>

---

## About Me

I'm a software engineer who thinks like a security engineer. I build production systems — backends, async pipelines, mobile apps — and design them with secure architecture from day one rather than bolting it on later.

Graduating from Arizona State University in May 2026 and starting my Master's in Cybersecurity at Georgia Tech (Information Security track) in Fall 2026. My focus:

- **Application security** — threat modeling, secure-by-default architecture, AI/LLM hardening
- **DevSecOps** — embedding SAST, SCA, secret scanning, and SARIF-driven merge gates into CI/CD
- **Full-stack engineering** — APIs, async pipelines, offline-first mobile, data-layer security

---

## Experience

### Software Engineering Intern @ [LinkClicks](https://linkclicks.io) — [3dsearch.org](https://3dsearch.org/)
`Python` `Django` `React` `PostgreSQL` `GitHub Actions`

> Aug 2025 – May 2026 · Remote · contributor on a multi-developer team

- Built a **3-layer prompt-injection defense** modeled on OWASP LLM01 (sanitization, label wrapping, output validation), blocking credential leakage, SQL fragments, and script tags across the integrated AI features
- Implemented a **Trivy-based GitHub Actions DevSecOps pipeline** gated on HIGH/CRITICAL findings — caught 3 real CVEs pre-merge over the project's lifetime
- Engineered a **token-bucket rate limiter** (sync/async, exponential backoff, Retry-After honoring) shielding 5 third-party scraper integrations from API bans; covered by 8 pytest cases

---

## Featured Projects

### [LLM Vulnerability Scanner](https://github.com/Just-In-N-Out/LLM-Vulnerability-Scanner) — AI/LLM Scanner + DevSecOps Pipeline
`Python` `asyncio` `GitHub Actions` `SARIF` `Pydantic` `OWASP LLM Top 10`

- **Deterministic rule engine** (18 rules across 4 OWASP LLM Top 10 categories) that replaced an LLM-as-judge evaluator — flagging credential leakage, prompt-injection persona hijacks, and XSS/SQLi/shell payloads in model output; backed by 103 passing tests
- **Canary-token defense** that injects a per-scan secret into the target's system prompt and detects verbatim exfiltration for a high-precision prompt-leak signal, tuned to ignore legitimate refusals
- **Async (asyncio/httpx) attack client** for Gemini, OpenAI, and Ollama, packaged into a reusable GitHub Actions matrix (Bandit, Semgrep, pip-audit) emitting SARIF 2.1.0 to the GitHub Security tab behind a merge-blocking severity gate

### [MinimaLog](https://github.com/Just-In-N-Out/MinimaLog) — iOS Workout Tracking App
`TypeScript` `React` `Capacitor` `Supabase` `PostgreSQL` — [minimalog.fit](https://minimalog.fit)

- **Offline-first sync engine** queuing mutations in an encrypted IndexedDB store and reconciling with Supabase/Postgres on reconnect — sequencing dependent operations and resolving temporary client IDs to server UUIDs
- **Database-layer authorization** across 20+ PostgreSQL tables with Row-Level Security to eliminate IDOR risk; hardened the data layer by revoking client-role EXECUTE on privileged RPCs and pinning function `search_path`
- **Client-side encryption** (WebCrypto AES-256-GCM, PBKDF2-derived keys at 100k iterations) protecting cached auth tokens at rest with an iOS WebView fallback, plus HMAC-SHA256-verified third-party webhooks
- **OAuth 2.0 PKCE** with an exact-match redirect/scheme allowlist blocking open-redirect attacks on native deep-link callbacks

### [DevSecOps Pipeline](https://github.com/Just-In-N-Out/devsecops-pipeline) — Reusable CI Security Pipeline
`GitHub Actions` `Bash` `SARIF`

- **Reusable GitHub Actions pipeline** fanning out to 6 parallel scan stages (secrets, SAST, dependency CVEs, IaC, container, SBOM) across 5 scanners, all normalized to SARIF in the GitHub Security tab
- **Bash severity gate** enforcing merge-blocking thresholds with a fingerprint baseline-diff (excludes line numbers, so findings survive rebases) — legacy repos onboard without blocking on inherited findings; unscored Gitleaks secret leaks reclassified as critical
- Language auto-detection (Python/Node/Go/Java), 6 configurable inputs, dependency-free HTML report; 5 semver releases plus a self-test running the pipeline against its own codebase

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
