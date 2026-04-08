# Resolve AI — Positioning Document
*Synthesized from: Listening Tour, Messaging House FY27 Q1, ADP Q&A, Demo Talk Track, Product Spec, Customer Stories*
*Last updated: April 7, 2026*

---

## Executive Summary

Resolve AI is the **production intelligence platform** that closes the loop from alert to root cause — automatically, across every tool in the stack, with evidence engineers can trust. Where all prior solutions required engineers to do the work of figuring out what's going on, Resolve has built the AI agent layer that does that work for them.

The thesis in one line: **Most of the time your engineering team loses isn't from fixing issues — it's from figuring out what's going on.**

---

## 1. Competitive Alternatives — What Would They Do Without Us?

When an alert fires and production breaks, engineering teams today face three alternatives, each with a critical ceiling:

**Alternative A: Manual, multi-tool investigation**
The status quo. Engineer gets paged, opens 4–6 dashboards, queries Splunk, checks Kubernetes, pings the person who "owns" that service, starts a war room, and 30–90 minutes later assembles a theory about what happened. This is the default at most enterprises. It works — slowly. Every incident starts from scratch. Tribal knowledge lives in three people's heads, and when they're not on call, the bridge call runs long.

**Alternative B: Native AI features in single observability vendors (Datadog AI, Splunk AI, etc.)**
These tools add AI to their own data silo. If an incident spans Splunk logs, Kubernetes state, and a recent deployment, no single vendor's AI can investigate across all three. They reduce noise within their platform; they don't close the loop across the stack. The customer already owns the observability stack — this doesn't change how hard it is to stitch it together.

**Alternative C: DIY Claude + MCP + internal skills/runbooks**
The emerging build-vs-buy alternative. Teams can automate narrow, single-engineer debugging tasks with a Claude wrapper and custom tools. Early results look promising. But this approach reaches a wall between months 3–6: it breaks down when problems cross team boundaries, when governance degrades as multiple teams modify prompts independently, and when persistent organizational knowledge is needed at scale. It gets teams to ~60% of the solution. DoorDash evaluated this path and walked away. A global hedge fund eliminated its dedicated NOC role by choosing Resolve instead.

**What none of these can do:** Run a simultaneous, multi-signal investigation across the full stack, rank multiple working theories with evidence, surface the causal chain in 90 seconds, and make that output available to every engineer — not just the three who know the system. That's the gap Resolve is built to own.

---

## 2. Unique Attributes — What Does Resolve Have That No One Else Does?

### Cross-Stack Agent Swarm
Resolve deploys a coordinated swarm of specialized AI agents that simultaneously query logs (Splunk, Loki, Elasticsearch), metrics (Datadog, Prometheus, Grafana, Cortex), traces (Jaeger, Tempo, OpenTelemetry), infrastructure state (Kubernetes, AWS, GCP), deployment history (GitHub, GitLab, ArgoCD), and runbooks (Confluence, Notion) — in parallel, at the moment an alert fires. No human pivot. No single-vendor constraint. The result is a structured investigation with ranked working theories, evidence, and a probable root cause — delivered before the war room starts.

**So what?** Engineers start incidents with answers instead of questions. The first hour of every incident — triage, correlation, context-gathering — is done before they open a dashboard.

### Post-Trained Models on Real Production Patterns
Resolve's AI is not generic LLM reasoning applied to observability. The models are post-trained on real incident patterns across production deployments at DoorDash, Coinbase, Zscaler, and dozens of other engineering organizations. There is also a continuous eval loop that improves accuracy over time in each customer environment. This is the compounding flywheel: every investigation Resolve runs makes the next one faster and more precise.

**So what?** This is why Resolve can rank working theories by confidence and explain why one is more likely than another — something generic LLM tools cannot do reliably at production scale.

*Founded by the creators of OpenTelemetry — the open standard for observability data. The AI team includes former Google DeepMind engineers who built Deep Research agents for Gemini.*

### Organizational Intelligence Layer — The "Multiplayer" Moat
Skills and Claude+MCP are single-player: one engineer, one alert, one local context. Resolve is multiplayer. It captures and maintains a living organizational knowledge layer — service ownership maps, known failure modes, runbook locations, escalation paths, team context — that is shared across every engineer and every agent investigation. This organizational layer is what breaks down for all competitors: it can't be replicated by a vendor AI locked to one tool, and it can't be maintained by an internal skills build that lives in individual engineers' heads.

**So what?** Every time a key engineer leaves, their production IP persists in Resolve. The 30-engineer war room shrinks because anyone — not just the person who "owns" that service — can start with full context.

### Evidence-Backed Causal Chain, Not Black Box Output
Every Resolve investigation exposes the full reasoning chain: which queries were executed, which data sources were queried, what each finding means, and how confidence was calculated. Engineers can drill into any claim. The output is not a guess — it's a defensible, citable diagnosis. Engineers can ask follow-up questions mid-investigation in natural language, and the whole team can work the same investigation simultaneously.

**So what?** Adoption doesn't require blind trust in AI. Engineers engage with Resolve the way they engage with a senior teammate — they interrogate its conclusions and build on them.

### Satellite Architecture — Security-First Design
A lightweight Satellite agent deploys inside the customer's environment. All connections are outbound-only from the Satellite to Resolve's cloud — no inbound access, no raw log storage in Resolve's cloud, full TLS encryption in transit. Sensitive data (PII, CII, cardholder data) is redacted at the Satellite layer before it leaves the environment. Resolve holds SOC 2 Type II (2025) and has completed security reviews for Nasdaq, Morgan Stanley, Salesforce, and ADP.

**So what?** The security objection — the most common enterprise blocker — is structurally resolved by design, not by negotiation. This is why Resolve wins in financial services and regulated environments.

---

## 3. Value for Customers — What Does This Enable?

### For On-Call Engineers: Get to Root Cause Before the War Room Starts
- DoorDash Ads: 87% faster root cause identification. Investigation time from 40 minutes to under 5 minutes in measured cases.
- Coinbase: 72% reduction in investigation time. Root cause in under 10 minutes. 250+ weekly investigation sessions across 100+ engineers — Resolve became the default investigation surface.
- Zscaler: 75% reduction in investigation time. 30% fewer engineers per incident. 100% of 150,000+ monthly alerts investigated.
- Fortune 50 Enterprise Software Company: 60–80% MTTR reduction across connected services. Time-to-root-cause in minutes rather than hours at a company logging 160,000 investigation hours annually.
- Uni (India): 65% improvement in MTTR, 2x developer productivity, 25% improvement in service reliability.
- Blueground: 4x faster root cause. Incidents that took 20+ minutes now resolve in under 5.

**The common thread:** Engineers stop losing the first hour of every incident to triage, correlation, and context-gathering. They start incidents with an answer instead of a blank page.

### For Engineering Leaders: Protect Reliability as Shipping Velocity Increases
AI coding tools are accelerating code output. More code in production means more surface area, more dependencies, more incidents — for the same on-call rotation. Engineering leaders who invest only in AI for development are solving the easier half. The orgs winning at AI-native engineering have applied AI to production as well. Resolve is the production layer that keeps reliability from becoming the ceiling on engineering velocity.

### For CTOs and VPs Engineering: The Institutional Memory That Doesn't Leave
Production knowledge — how systems actually behave under stress, which failure modes recur, what the blast radius of a config change is — lives in the heads of 2–3 senior engineers at most organizations. When they're on vacation, the bridge runs long. When they leave, the IP leaves. Resolve captures this knowledge continuously and makes it available to every engineer and every agent at the moment it's needed. The team gets stronger, not just bigger.

---

## 4. Target Customers — Who Cares Most About This?

### Primary ICP: Service Owners at Engineering-Led Companies

**The right entry persona is not SRE or platform engineering.** SRE and platform teams build infrastructure and get escalated to — they don't own services end-to-end and can't drive a POC to completion without pulling in every app team. The right first call is the **service owner or application owner**: the engineering manager or senior engineer who writes the code, owns the on-call rotation for their service, and feels the full weight of MTTR.

**Company profile:**
- 200–5,000 engineers
- Engineering-driven business where production reliability has direct revenue or customer impact (fintech, crypto, marketplace, SaaS infrastructure, enterprise software)
- Already owns the observability stack: Datadog, Splunk, or both; plus Kubernetes, PagerDuty, GitHub/GitLab
- Has an active on-call culture with measurable alert volume and escalation patterns
- Has an AI mandate at the VP+ level — an executive sponsor driving AI adoption across engineering

**The buying trigger:**
One or more of: a painful postmortem or P0 incident that exposed an investigation gap; on-call burnout reaching a breaking point; a high-priority engineer departure; leadership pressure to show AI ROI across engineering (not just coding tools); or an AI OKR with budget attached.

**The wrong first call:**
Platform/infrastructure teams without service ownership. They feel organizational pain, not investigation pain. They care about the vision but can't be the POC champion without pulling in 10 other teams — and that creates the 20-meeting scoping death march.

### Secondary ICP: CTOs / VP Engineering at AI-Forward Companies
Executive buyers who are past "should we use AI?" and are asking "how do we deploy AI across our entire engineering organization?" These leaders understand that AI for development is table stakes; they're looking for the production counterpart. They respond to: organizational knowledge capture, agent-first on-call design, and the vision of engineering orgs where production is self-explanatory. They sign deals; they don't run POCs. Their champion is the on-the-line manager one layer below them.

---

## 5. Market Category — What Game Are We Playing?

### The Insertion Category: AI Incident Response Automation
This is the box customers want to put Resolve in — and it's the right box for creating urgency and driving evaluation. It's specific, time-pressured, and measurable. The objection "we already have [Datadog / Splunk AI]" is answered directly: native AI only works within one vendor's data. Resolve operates across the full stack. Win this category and you have a customer. Own this category and you have a growth engine.

**One-line: Resolve is the AI layer that closes the loop from alert to root cause — across every tool in your stack, automatically.**

### The Vision Category: Production Intelligence Platform
This is the board-level, multi-year framing. Engineering organizations are evolving from human-run operations to agent-assisted production. The question is: who builds the organizational intelligence layer that makes agentic debugging possible at scale — across teams, across services, across time? Claude+skills is single-player and local. Datadog AI is single-vendor. Resolve is the cross-team, cross-stack platform that becomes the production operating system for AI-native engineering organizations.

**One-line: Resolve is the production intelligence platform that makes every engineer — and every AI agent — as effective as your best SRE.**

---

## 6. Messaging Architecture — Two Altitudes, One Story

### Altitude 1 — Insertion Messaging (Creates Urgency, Drives Evaluation)
*Use with: AEs in first calls, SDR outbound, field marketing, conference talks*

> "Most of the time your engineering team loses isn't from fixing issues — it's from figuring out what's going on. Resolve AI closes the loop from paged alert to root cause automatically, across your entire stack, so your engineers start incidents with answers instead of questions."

**Proof:** DoorDash: 87% faster. Coinbase: 72% faster. Zscaler: 30% fewer engineers per incident.

### Altitude 2 — Vision Messaging (Expands Deal Size, Drives Exec Alignment)
*Use with: CTO/VP outreach, exec QBRs, category positioning, investor narrative*

> "AI coding tools help your team ship faster. But production is where the velocity goes to die — not because fixing things is hard, but because figuring out what's going on still falls on your best engineers, at 2am, starting from scratch every time. Resolve is the AI for production: the organizational intelligence layer that makes every engineer and every agent as effective as your best SRE."

**Proof:** Fortune 50 enterprise software company: 160,000 hours/year in investigation time reduced. Production knowledge accessible in seconds, not locked in three people's heads.

---

## 7. Competitive Differentiation — The Battlecard Summary

| Competitor | What They Do | Where They Fall Short | Resolve's Answer |
|---|---|---|---|
| **Datadog AI / Splunk AI** | AI within their own data silo | Can't investigate across multi-vendor stacks | Cross-stack agent swarm across 100+ integrations |
| **IBM AIOps / PagerDuty AIOps** | Alert correlation and grouping | Correlation ≠ root cause. No autonomous investigation | Structured diagnosis with evidence, not just grouped alerts |
| **Claude + MCP + skills** | Single-engineer task automation | Breaks down at team boundaries, knowledge doesn't persist, no governance at scale | Organizational intelligence layer — multiplayer, not single-player |
| **Internal build** | Full control | Requires AI research investment (evals, knowledge graphs, governance) that compounds faster than a sprint team can maintain | 2+ years, $150M, post-trained on real production patterns. DoorDash evaluated and walked away. |
| **Generic observability (Grafana, New Relic)** | Visibility | Visibility ≠ investigation. Engineers still have to stitch it together | Resolve sits above observability tools — it uses them, doesn't replace them |

---

## 8. Proof Point Architecture

### The Headline Stats (Use Liberally)
- **87%** faster root cause identification — DoorDash Ads
- **72%** faster investigation time — Coinbase
- **75%** reduction in investigation time; **30%** fewer engineers per incident — Zscaler
- **60–80%** MTTR reduction — Fortune 50 Enterprise Software Company
- **4x** faster time to root cause — Blueground, Uni
- **100%** of alerts investigated — Zscaler, Uni, Blueground
- **250+** investigation sessions/week across 100+ engineers — Coinbase

### The Narratives (Use for Executive Conversations)
- **DoorDash:** One incident, Resolve identified root cause in 15 minutes. Engineer took a different path, returned 105 minutes later to Resolve's original finding — which was correct. On a $1B+ ads platform, that gap represents up to $200K in potential revenue exposure.
- **Coinbase:** "Writing code is no longer the bottleneck." Engineering lead said it publicly at re:Invent. 120M+ users, complex microservices, Resolve became the default investigation surface for the entire SRE org.
- **Fortune 50:** 160,000 hours of investigation time annually across the engineering org. One team alone logged 2,000+ service interruption hours in eight months — not from lack of capability, but from the complexity of cross-team signal correlation. Resolve delivered 60–80% MTTR reduction at scale.
- **Build vs. Buy (DoorDash):** Evaluated building their own. Technically feasible, economically impractical. Tens of engineers, continuous fine-tuning, and capacity pulled away from customer-impacting work. They walked away.

### Team Credibility
- Founded by the creators of **OpenTelemetry** (the open standard for observability data)
- AI team includes former **Google DeepMind** engineers who built Deep Research agents for Gemini
- **$150M raised at a $1B valuation** — more than all competitors in this space combined
- SOC 2 Type II (2025); completed security reviews for Morgan Stanley, Nasdaq, Salesforce, ADP

---

## 9. Positioning Quality Checks

| Test | Result |
|---|---|
| **Uniqueness Test** — Could a competitor say the same thing? | Cross-stack post-trained agent swarm with multiplayer organizational intelligence: **NO competitor can make this claim** |
| **Evidence Test** — Every claim backed? | All primary claims anchored to DoorDash, Coinbase, Zscaler, Fortune 50 customer outcomes |
| **"So What?" Test** — Every feature linked to buyer value? | Yes — each attribute section states the buyer-level implication |
| **Language Test** — Uses ICP language? | "War room," "bridge call," "paged at 2am," "tribal knowledge," "on-call toil" — language sourced from actual customer conversations |
| **"AI SRE" Warning** | Avoid as primary label — confirmed problematic in Listening Tour. Use "AI incident response automation" at insertion altitude, "production intelligence platform" at vision altitude |

---

## 10. What to Say When…

**"We already have Datadog AI / Splunk AI"**
> Those tools do AI within their data silo. When an incident spans Splunk logs, Kubernetes state, and a recent deployment, no single vendor's AI can investigate across all three. Resolve operates across your full stack, regardless of which tools you use.

**"Can't we just build this with Claude + skills?"**
> You can get to a prototype fast. The wall hits between months 3–6: cross-team incidents, persistent knowledge, reliability at scale. DoorDash evaluated that path and walked away. A global hedge fund eliminated a dedicated NOC role by choosing Resolve instead. The difference isn't model quality — it's organizational architecture.

**"How is this different from AIOps?"**
> AIOps correlates and groups alerts. Resolve investigates. When Resolve finishes, you have a causal chain with evidence — not a cluster of related alerts. You know what happened and why.

**"We need to see it work on our environment before we commit"**
> That's exactly the right instinct, and it's how we structure every POC. We don't demo on sanitized data — we connect to your stack, run investigations on live alerts, and let results speak. The typical POC runs 8–10 weeks: 2 weeks integration, 4 weeks calibration, 4 weeks live evaluation against your KPIs.

---

*Sources: Resolve AI Listening Tour (Pawan Shankar, April 2026) | Resolve AI Messaging House FY27 Q1 | ADP x Resolve AI Technical Q&A | Demo Talk Track | Feb 2026 Product Spec | Customer case studies: DoorDash, Coinbase, Zscaler, Fortune 50, Uni, Blueground*
