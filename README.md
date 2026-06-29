<!-- Intended repo: github.com/jakob-prince/jakob-prince  (file: README.md) -->
<!-- This is your GitHub *profile* README — it renders at the top of github.com/jakob-prince -->

### Hi, I'm Jakob 👋

I build AI-native systems — and I build them *with* AI. My focus is designing
the architecture, invariants, and guardrails that make AI-in-the-loop software
reliable, then shipping it fast by pairing with coding agents.

I work at the intersection of go-to-market and engineering: turning messy,
real-world workflows into clean, event-driven systems with AI doing the
judgment-heavy parts.

---

## Featured projects

### 1 · [llm-eval-playground](https://github.com/jakob-prince/llm-eval-playground)
> Run one prompt across multiple LLMs side-by-side and score every output against a weighted rubric.

[![CI](https://github.com/jakob-prince/llm-eval-playground/actions/workflows/ci.yml/badge.svg)](https://github.com/jakob-prince/llm-eval-playground/actions/workflows/ci.yml)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-Streamlit-FF4B4B?logo=streamlit&logoColor=white)](https://llm-eval-playground-hbhkccgv2ynxoj9xz2ht2v.streamlit.app/)

**▶ [Try it live](https://llm-eval-playground-hbhkccgv2ynxoj9xz2ht2v.streamlit.app/)** — boots on built-in fake models, no API key required; paste your own key (session-only) to run real providers.

A Streamlit eval harness with a clean pure-Python core: `ModelAdapter` protocol (OpenAI / Anthropic / fake), `Judge` protocol (LLM-as-judge or deterministic fake for CI), and a weighted rubric scorer — all composed by a thin UI shell. mypy strict, 9 tests on fakes, CI-green.

---

### 2 · [ratelimit-proxy](https://github.com/jakob-prince/ratelimit-proxy)
> Async HTTP client library: token-bucket rate limiter + exponential-backoff retry + pluggable TTL cache.

[![CI](https://github.com/jakob-prince/ratelimit-proxy/actions/workflows/ci.yml/badge.svg)](https://github.com/jakob-prince/ratelimit-proxy/actions/workflows/ci.yml)

Production reliability primitives for outbound HTTP calls, written as a composable async Python library. `TokenBucket` releases its asyncio lock during sleep so competing coroutines proceed; `RetryPolicy` uses full jitter + `Retry-After` header; `CacheBackend` is a pluggable protocol (swap in Redis). Clock and sleep are injectable so 45 tests run entirely on fakes — no real network, no real sleeps. mypy strict, CI-green.

---

### 3 · [behavior-triggered-outreach-engine](https://github.com/jakob-prince/behavior-triggered-outreach-engine)
> A sanitized reference implementation of a behavior-triggered, AI-personalized PLG outreach pattern.

[![CI](https://github.com/jakob-prince/behavior-triggered-outreach-engine/actions/workflows/ci.yml/badge.svg)](https://github.com/jakob-prince/behavior-triggered-outreach-engine/actions/workflows/ci.yml)

Detect → exclude → score → cohort → AI-draft → enroll. Each stage is a pure function; AI and CRM sit behind swappable interfaces so the pipeline is testable end-to-end on synthetic data. Demonstrates how to design AI-in-the-loop systems with deterministic invariants at the seams.

---

**What these show together:** clean async Python, testing discipline (fakes over mocks, injectable dependencies, no real I/O in tests), AI-native workflow design, and the ability to ship a deployed, interactive demo.

**How I build:** I architect the system and its invariants, then move fast with AI coding agents — and I can walk through every design tradeoff live.

---

**What I care about**
- 🧠 AI-in-the-loop system design — knowing *what* to hand the model and *where* to keep deterministic guarantees
- 🧩 Clean architecture — pure functions, swappable interfaces, tested invariants
- ⚡ Building fast with coding agents, then being able to defend every decision

📫 [LinkedIn](https://www.linkedin.com/in/jakobprince/) · open to demo speakerships and technical conversations
