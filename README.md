# Hi, ich bin CO-Vice 👋

**Oliver Weiss** · Co-Founder & Builder agentischer Plattformen · Hamburg

[![LinkedIn](https://img.shields.io/badge/LinkedIn-oliweiss-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/oliweiss)
[![E-Mail](https://img.shields.io/badge/E--Mail-o.weiss%40guidedpathadvisors.com-D14836?logo=gmail&logoColor=white)](mailto:o.weiss@guidedpathadvisors.com)
[![Jack Rabbit](https://img.shields.io/badge/jack--rabbit.ai-Culture%20Intelligence-111827)](https://jack-rabbit.ai)

15 Jahre Go-to-Market, Growth und P&L-Verantwortung (Criteo, Sizmek, Adform, Microsoft). Dann der Seitenwechsel in den Maschinenraum: Seit 18 Monaten baue und betreibe ich als Co-Founder zwei mandantenfähige, agentische KI-Plattformen – nicht als der Gründer, der Wünsche in Jira ablädt, sondern als der, der nachts das Repo offen hat.

---

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

---

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

---

## Tech Stack

**Sprachen & Runtime**

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

**Backend & Daten**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Neon](https://img.shields.io/badge/Neon-00E599?logo=neon&logoColor=black)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?logo=supabase&logoColor=white)
![Drizzle](https://img.shields.io/badge/Drizzle_ORM-C5F74F?logo=drizzle&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Fastify](https://img.shields.io/badge/Fastify-000000?logo=fastify&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?logo=zod&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?logo=googlebigquery&logoColor=white)

**KI & Agenten**

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

## Zusammenarbeit

Wenn ihr genau zwischen „der Pilot läuft prima" und „die IT verweigert das Go-Live" feststeckt, begleite ich euch in drei Formaten:

| Format | Für wen | Ergebnis |
|---|---|---|
| **Agent Production Readiness Audit** · 10 Tage, Festpreis | Mittelstand und Scale-ups, deren Agenten-Pilot seit Wochen nicht produktiv geht | Eval-Set für die 20 kritischsten Fälle, Governance-Karte für das Management, Kostenprofil aus euren Logs, ein umgesetzter Quick-Win im Code, 90-Tage-Plan |
| **AI-native Engineering Enablement** · 3 Wochen, Festpreis | Dev-Teams (5–40), die Coding-Agenten einführen oder schon nutzen | `AGENTS.md`-Betriebsvertrag, deterministische CI-Gates, Cross-Model-Verifikation, Kosten-Baseline, Lern-Register – laufend im eigenen Repo |
| **Fractional Head of AI-GTM** · 2 Tage/Woche | Seed- und Series-A-Startups mit B2B-KI-Produkt und ohne besetzte GTM-Rolle | Positionierung, Pricing bei variablen Token-Kosten, Pilot-to-Paid-Playbook, CISO-feste Sales-Argumente |

Details und Konditionen: [LinkedIn](https://www.linkedin.com/in/oliweiss) oder direkt per [E-Mail](mailto:o.weiss@guidedpathadvisors.com).

---

<sub>Alle Kennzahlen stammen aus den Repositories der beiden Plattformen, Stand September 2026. Die Plattform-Repos sind proprietär; hier gibt es keinen Quellcode aus ihnen.</sub>
