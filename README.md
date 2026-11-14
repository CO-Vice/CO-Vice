# Hi, ich bin CO-Vice 👋

**Oliver Weiss** · Co-Founder & Builder agentischer Plattformen · Hamburg

[![LinkedIn](https://img.shields.io/badge/LinkedIn-oliweiss-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/oliweiss)
[![E-Mail](https://img.shields.io/badge/E--Mail-o.weiss%40guidedpathadvisors.com-D14836?logo=gmail&logoColor=white)](mailto:o.weiss@guidedpathadvisors.com)
[![Jack Rabbit](https://img.shields.io/badge/jack--rabbit.ai-Culture%20Intelligence-111827)](https://jack-rabbit.ai)

🇩🇪 **[Deutsch](#-deutsch)** · 🇬🇧 **[English](#-english)**

---

# 🇩🇪 Deutsch

25 Jahre Go-to-Market, Growth und P&L-Verantwortung (Criteo, Sizmek, Adform, Microsoft). Dann der Seitenwechsel in den Maschinenraum: Seit 18 Monaten baue und betreibe ich als Co-Founder zwei mandantenfähige, agentische KI-Plattformen – nicht als der Gründer, der Wünsche in Jira ablädt, sondern als der, der nachts das Repo offen hat.

## Über mich

Ich arbeite an der Stelle, an der KI-Piloten scheitern: zwischen dem Fachbereich, der Ergebnisse will, und IT, Legal und CISO, die nach Tenant-Isolation, Kosten und Haftung fragen. Mein Kern ist deshalb weniger „Prompt Engineering" als **Betriebsfähigkeit**:

- **Agentische Systeme in Produktion** – LLM-Orchestrierung mit Modell-Registry, Fallbacks und versionierten Prompts; jeder Modellaufruf läuft durch Rate-Limit und Metering mit Budget-Check pro Use-Case.
- **Multi-Tenant-Backends** – Postgres mit Tenant-Isolation (als ADR entschieden und mit echten DB-Integrationstests abgesichert), Billing, Job-Control-Plane für selbststeuernde Datenaufnahme, Observability mit Sentry/Pino.
- **Governance für agentische Entwicklung** – ein Betriebsvertrag (`AGENTS.md`), den jeder Coding-Agent liest, bevor er Code oder Daten anfasst; deterministische CI-Gates und Hooks; Cross-Model-Verifikation jedes materiellen Commits durch einen zweiten Modellanbieter ohne Mocks; ein Lern-Register, dessen wiederholte Einträge zu Regeln oder Tests werden.
- **Token-Economics als Code** – Kontext- und Effort-Policy aus gemessenen Sessions abgeleitet, nicht aus Bauchgefühl.

### Drei Lektionen aus 18 Monaten Plattformbau

1. **Der Agent ist nicht das Produkt. Das Regelwerk ist es.**
2. **Ein grüner Test beweist gar nichts – bis er einmal gebrochen wurde.**
3. **Was ein Agent kostet, entscheidet über das Produkt. Nicht die Inferenz-Infrastruktur.**

### Zahlen aus den Repositories (Stand September 2026)

| | |
|---|---|
| **3.466** | Commits in 12 Monaten |
| **2.322** | Testdateien, davon echte DB-Integrationstests |
| **23** | Architecture Decision Records im Code |
| **8** | Modellanbieter, die sich gegenseitig verifizieren |
| **100 %** | der Modellaufrufe mit Rate-Limit und Metering |
| **53 % → gekappt** | Anteil der Agenten-Sessions über 200k Kontext – gemessen, dann per Policy begrenzt |

## Aktuelle Projekte

Die Plattformen sind proprietär und nicht öffentlich. Hier das Schaufenster – was ich baue, nicht wie es intern aussieht.

### Jack Rabbit Culture Decoder · Production
Culture-Intelligence-Plattform, die misst, wie kulturell relevant eine Marke tatsächlich ist – für Menschen und für KI-generierte Antworten. Im Kern: Next.js/TypeScript-Anwendung auf Neon Postgres mit Tenant-Isolation, LLM-Pipeline über das Vercel AI SDK mit Metering und Budget-Grenzen, Inngest-Jobs für die Datenaufnahme, Stripe-Billing, Sentry/Pino-Observability, Vitest-Integrationstests gegen echte Datenbanken und Playwright-E2E.

### Guided Path Navigator (GPN) · Production
Agentische B2B-Plattform für Marktanalyse und Vertriebs-Intelligence. Monorepo mit Next.js-Frontend, Node-API und einem Python-Backend (FastAPI, LangGraph/LangChain) für die Agenten-Orchestrierung; mehrere LLM-Anbieter mit Fallbacks, pgvector für semantische Suche, Docker-Compose-Deployment inklusive lokaler Inferenz (Ollama/vLLM).

### Jack Rabbit Leads · Production
Lead-Intelligence-Service: Verticals- und ICP-Modelle, Anreicherung über externe Datenquellen, Queue-basierte Verarbeitung (BullMQ) und Partner-Reports. Express/TypeScript-Backend mit Drizzle auf Postgres, React-Client, Anthropic SDK, BigQuery.

### Nebenbei
- **[handball-heimspiele](https://github.com/CO-Vice/handball-heimspiele)** – kleines privates Tool, das Heimspiele hochklassiger Handball-Teams im Umkreis findet. Spielerei, aber öffentlich.

## Zusammenarbeit

Wenn ihr genau zwischen „der Pilot läuft prima" und „die IT verweigert das Go-Live" feststeckt, begleite ich euch in drei Formaten:

| Format | Für wen | Ergebnis |
|---|---|---|
| **Agent Production Readiness Audit** · 10 Tage, Festpreis | Mittelstand und Scale-ups, deren Agenten-Pilot seit Wochen nicht produktiv geht | Eval-Set für die 20 kritischsten Fälle, Governance-Karte für das Management, Kostenprofil aus euren Logs, ein umgesetzter Quick-Win im Code, 90-Tage-Plan |
| **AI-native Engineering Enablement** · 3 Wochen, Festpreis | Dev-Teams (5–40), die Coding-Agenten einführen oder schon nutzen | `AGENTS.md`-Betriebsvertrag, deterministische CI-Gates, Cross-Model-Verifikation, Kosten-Baseline, Lern-Register – laufend im eigenen Repo |
| **Fractional Head of AI-GTM** · 2 Tage/Woche | Seed- und Series-A-Startups mit B2B-KI-Produkt und ohne besetzte GTM-Rolle | Positionierung, Pricing bei variablen Token-Kosten, Pilot-to-Paid-Playbook, CISO-feste Sales-Argumente |

Details und Konditionen: [LinkedIn](https://www.linkedin.com/in/oliweiss) oder direkt per [E-Mail](mailto:o.weiss@guidedpathadvisors.com).

Der Tech Stack steht [weiter unten](#tech-stack).

---

# 🇬🇧 English

15 years of go-to-market, growth and P&L responsibility (Criteo, Sizmek, Adform, Microsoft). Then I switched sides into the engine room: for the past 18 months I have been building and operating two multi-tenant, agentic AI platforms as a co-founder – not the founder who drops wishes into Jira, but the one who has the repo open at night.

## About me

I work at the exact point where AI pilots fail: between the business unit that wants results and IT, Legal and the CISO who ask about tenant isolation, cost and liability. So my core is less "prompt engineering" than **operability**:

- **Agentic systems in production** – LLM orchestration with a model registry, fallbacks and versioned prompts; every model call passes through rate limiting and metering with a per-use-case budget check.
- **Multi-tenant backends** – Postgres with tenant isolation (decided as an ADR and secured with real DB integration tests), billing, a job control plane for self-steering data ingestion, observability with Sentry/Pino.
- **Governance for agentic development** – an operating contract (`AGENTS.md`) that every coding agent reads before touching code or data; deterministic CI gates and hooks; cross-model verification of every material commit by a second model provider, without mocks; a learnings register whose repeated entries become rules or tests.
- **Token economics as code** – context and effort policies derived from measured sessions, not gut feeling.

### Three lessons from 18 months of platform building

1. **The agent is not the product. The rulebook is.**
2. **A green test proves nothing – until it has been broken once.**
3. **What an agent costs decides the product. Not the inference infrastructure.**

### Numbers from the repositories (as of September 2026)

| | |
|---|---|
| **3,466** | commits in 12 months |
| **2,322** | test files, including real DB integration tests |
| **23** | Architecture Decision Records in the codebase |
| **8** | model providers verifying each other |
| **100 %** | of model calls with rate limiting and metering |
| **53 % → capped** | share of agent sessions above 200k context – measured, then limited by policy |

## Current projects

The platforms are proprietary and not public. This is the showcase – what I build, not how it looks inside.

### Jack Rabbit Culture Decoder · Production
Culture intelligence platform that measures how culturally relevant a brand really is – for people and for AI-generated answers. At its core: a Next.js/TypeScript application on Neon Postgres with tenant isolation, an LLM pipeline via the Vercel AI SDK with metering and budget limits, Inngest jobs for data ingestion, Stripe billing, Sentry/Pino observability, Vitest integration tests against real databases and Playwright E2E.

### Guided Path Navigator (GPN) · Production
Agentic B2B platform for market analysis and sales intelligence. Monorepo with a Next.js frontend, a Node API and a Python backend (FastAPI, LangGraph/LangChain) for agent orchestration; multiple LLM providers with fallbacks, pgvector for semantic search, Docker Compose deployment including local inference (Ollama/vLLM).

### Jack Rabbit Leads · Production
Lead intelligence service: vertical and ICP models, enrichment from external data sources, queue-based processing (BullMQ) and partner reports. Express/TypeScript backend with Drizzle on Postgres, React client, Anthropic SDK, BigQuery.

### On the side
- **[handball-heimspiele](https://github.com/CO-Vice/handball-heimspiele)** – small private tool that finds home games of top-tier handball teams nearby. A toy, but public.

## Working together

If you are stuck exactly between "the pilot works fine" and "IT refuses the go-live", I support you in three formats:

| Format | For whom | Outcome |
|---|---|---|
| **Agent Production Readiness Audit** · 10 days, fixed price | Mid-market companies and scale-ups whose agent pilot has not reached production for weeks | Eval set for the 20 most critical cases, governance map for management, cost profile from your logs, one implemented quick win in code, 90-day plan |
| **AI-native Engineering Enablement** · 3 weeks, fixed price | Dev teams (5–40) introducing or already using coding agents | `AGENTS.md` operating contract, deterministic CI gates, cross-model verification, cost baseline, learnings register – running in your own repo |
| **Fractional Head of AI-GTM** · 2 days/week | Seed and Series A startups with a B2B AI product and no GTM role in place | Positioning, pricing with variable token costs, pilot-to-paid playbook, CISO-proof sales arguments |

Details and terms: [LinkedIn](https://www.linkedin.com/in/oliweiss) or directly by [e-mail](mailto:o.weiss@guidedpathadvisors.com).

---

## Tech Stack

**Languages & Runtime**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?logo=nodedotjs&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white)

**Frontend**

![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white)
![Radix UI](https://img.shields.io/badge/Radix_UI-161618?logo=radixui&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)

**Backend & Data**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Neon](https://img.shields.io/badge/Neon-00E599?logo=neon&logoColor=black)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?logo=supabase&logoColor=white)
![Drizzle](https://img.shields.io/badge/Drizzle_ORM-C5F74F?logo=drizzle&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Fastify](https://img.shields.io/badge/Fastify-000000?logo=fastify&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?logo=zod&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?logo=googlebigquery&logoColor=white)

**AI & Agents**

![Anthropic](https://img.shields.io/badge/Anthropic_Claude-191919?logo=anthropic&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?logo=openai&logoColor=white)
![Mistral](https://img.shields.io/badge/Mistral-FA520F?logo=mistralai&logoColor=white)
![Vercel AI SDK](https://img.shields.io/badge/Vercel_AI_SDK-000000?logo=vercel&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain_%2F_LangGraph-1C3C3C?logo=langchain&logoColor=white)
![MCP](https://img.shields.io/badge/Model_Context_Protocol-111827)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?logo=postgresql&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama_%2F_vLLM-000000?logo=ollama&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?logo=anthropic&logoColor=white)
![Codex](https://img.shields.io/badge/Codex-412991?logo=openai&logoColor=white)

**Jobs, Auth, Billing, Observability**

![Inngest](https://img.shields.io/badge/Inngest-000000)
![BullMQ](https://img.shields.io/badge/BullMQ-DC382D?logo=redis&logoColor=white)
![Auth.js](https://img.shields.io/badge/Auth.js-8B5CF6)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?logo=stripe&logoColor=white)
![Sentry](https://img.shields.io/badge/Sentry-362D59?logo=sentry&logoColor=white)
![Pino](https://img.shields.io/badge/Pino-687634)
![Upstash](https://img.shields.io/badge/Upstash-00E9A3?logo=upstash&logoColor=black)

**Testing, CI & Delivery**

![Vitest](https://img.shields.io/badge/Vitest-6E9F18?logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?logo=playwright&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?logo=pytest&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Turborepo](https://img.shields.io/badge/Turborepo-EF4444?logo=turborepo&logoColor=white)

---

<sub>DE: Alle Kennzahlen stammen aus den Repositories der beiden Plattformen, Stand September 2026. Die Plattform-Repos sind proprietär; hier gibt es keinen Quellcode aus ihnen.<br>EN: All figures come from the repositories of the two platforms, as of September 2026. The platform repos are proprietary; no source code from them is published here.</sub>
