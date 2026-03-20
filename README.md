<h1 align="center">Justin Issa</h1>
<h3 align="center">Security Engineer · Full-Stack Capable · AI/LLM Security</h3>

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-streak-stats-eight.vercel.app/?user=Just-In-N-Out&theme=tokyonight&hide_border=true&background=0D1117&stroke=00D4FF&ring=00D4FF&fire=FF6B35&currStreakLabel=00D4FF" />
    <source media="(prefers-color-scheme: light)" srcset="https://github-readme-streak-stats-eight.vercel.app/?user=Just-In-N-Out&hide_border=true&theme=default" />
    <img src="https://github-readme-streak-stats-eight.vercel.app/?user=Just-In-N-Out&hide_border=true" alt="GitHub Streak" />
  </picture>
</div>

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Just-In-N-Out&theme=github_dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Just-In-N-Out&theme=github" />
    <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Just-In-N-Out" alt="Profile Summary" />
  </picture>
</div>

---

## 🧠 About Me

I'm a security-focused engineer finishing my B.S. in Software Engineering at **Arizona State University** and pursuing a **Master's in Cybersecurity**. My edge is that I can go deep on the adversarial side and still ship production code.

My focus is the intersection of **AI systems and security** — specifically:

- 🔒 Securing LLM pipelines against prompt injection and adversarial inputs
- 🛡️ Designing secure backend architecture from the ground up — not patched after the fact
- 🔍 Red-teaming deployed AI systems for vulnerabilities

---

## 🚀 Featured Projects

### 🔍 [LLM Vulnerability Scanner](https://github.com/Just-In-N-Out) — Red-teaming tool for deployed LLMs
`Python` `FastAPI` `Typer`

- Systematically tests LLMs for prompt injection, jailbreaks, and system prompt extraction
- CLI + REST API interface for integration into security workflows

### 🔎 [3DSearch](https://github.com/Just-In-N-Out) — 3D model aggregator with LLM security layer
`Django` `PostgreSQL` `React` `Docker` `Ollama`

- Designed a three-layer prompt injection defense: input sanitization, structured prompt wrapping with labeled data blocks, and output validation that scans for API keys, SQL, and shell patterns
- Built a thread-safe token bucket rate limiter for external API calls alongside per-IP throttling — 100 req/hour with a global anonymous cap
- Custom exception middleware prevents information disclosure — generic errors returned to clients, full stack traces logged server-side only

### 🏋️ [MinimaLog](https://github.com/Just-In-N-Out/minimal-log) — Minimalist workout tracker
*Built because I wanted a no-nonsense way to track my lifts at the gym — every existing app was too bloated.*

`React` `TypeScript` `Capacitor` `Supabase`

- Row-Level Security on every user-facing table — nested ownership checks through `workout_exercises → workouts → user_id` prevent cross-user data access even with valid IDs
- SECURITY DEFINER server-side functions handle all sensitive aggregations and notifications — including self-notification prevention
- Zod schema validation on all user inputs — search queries restricted to alphanumeric, post/comment fields enforced with strict length and type bounds
- Mobile-first, available on iOS

*Built because I wanted a no-nonsense way to track my lifts at the gym.*

---

## 🛠️ Tech Stack

<div align="center">

**Languages & Frameworks**

<img src="https://skillicons.dev/icons?i=python,ts,js,react,django,fastapi" />

**Security & Infrastructure**

<img src="https://skillicons.dev/icons?i=kali,linux,bash,docker,aws,postgres,git" />

</div>

<div align="center">
  <img src="https://img.shields.io/badge/Burp_Suite-FF6633?style=for-the-badge&logo=burp-suite&logoColor=white" />
  <img src="https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white" />
  <img src="https://img.shields.io/badge/Metasploit-2596CD?style=for-the-badge&logo=metasploit&logoColor=white" />
</div>

---

## 🎯 Fun Facts

- 🏋️ I bench 265 lbs
- 🚩 I love doing Capture the Flag (CTF) challenges
- 🥋 Training jiu-jitsu (still getting submitted, but improving)
- 🍔 I love In-N-Out (yes, the username checks out)

---

## 🐍 My Contributions

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Just-In-N-Out/Just-In-N-Out/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Just-In-N-Out/Just-In-N-Out/output/github-contribution-grid-snake.svg" />
    <img alt="github-snake" src="https://raw.githubusercontent.com/Just-In-N-Out/Just-In-N-Out/output/github-contribution-grid-snake-dark.svg" />
  </picture>
</div>
