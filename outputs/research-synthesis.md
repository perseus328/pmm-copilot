# Research Synthesis
Generated: 2026-04-07
Documents ingested: 4
- `docs/positioning/EXAMPLE-current-positioning-v3.md` (example/placeholder positioning doc — AcmeObserve, not Resolve AI; structural reference only)
- `docs/competitors/competition.md` (internal competitive positioning doc: Resolve AI vs. observability platforms, incident platforms, AI SRE startups, DIY/Labs)
- `docs/calls/ticketmaster-first-call.md` (call note: S1 discovery call, Yevhen Zavhorodnii, Principal SRE, Ticketmaster)
- `outputs/attention-calls-pmm-analysis-s1-s4.md` (primary research: 25+ Resolve AI sales calls, Feb–Apr 2026, S1–S4, synthesized via Attention)

**Product:** Resolve AI — AI-powered incident investigation and root cause analysis for SRE/platform engineering teams
**Accounts covered:** LLoyds Banking Group, HSBC, TIAA, McKinsey, Adobe, DoorDash, Block/Square, ADT, Invisible, Upgrade, Bloom Credit, Salesforce, Ticketmaster

---

## Customer Voice Themes

### Theme 1: The Bridge Call Problem — Too Many People, Too Long to Resolve
The single most emotionally resonant pain is the overcrowded bridge call where engineers wait to be cleared. Ticketmaster echoes the same pattern (escalation to multiple teams, slow MTTR) that LBG and HSBC described.

> _"Reliability is not achieved. We have more failures and we want to reduce them. MTTR is high — meantime to resolution takes us a long time. Customers act as canaries so they find the problem before we do. Our incidents have 20+ engineers on a single bridge."_ — **Anestis Samaras, Group Head of Data Science, LBG**

> _"MTTR is high, customers are your canaries. So they report issues before you find them. And you have massive bridges with 20+ engineers on them."_ — **HSBC CTO/Service Management (S2 demo)**

> _"Not getting a result in 30 minutes is like holy crap."_ — **Brandon Zimmerman, Senior SRE, Block/Square (S3 POC)**

### Theme 2: Fragmented Tooling — No End-to-End Picture
Every account has a "zoo of systems." Ticketmaster runs Splunk, Kibana, Grafana, AWS/K8s, PagerDuty, FireHydrant, and GitHub — and gives teams autonomy, making standardization impossible.

> _"Our current environment is quite fragmented. We have different tools. There are some tools that don't have even basic observability at all. Some places we have Dynatrace, some places SignalFx, some places nothing."_ — **Jay Rudrachar, TIAA**

> _"The number biggest problem that we have is each team sort of understands what the challenges are, but we don't have the end-to-end picture."_ — **TIAA Operations leader**

> _"What we don't have is a mature resolve capability where we know what's happening, what is broken, but we do not know why and how to go about it. That's where we spend the majority of time."_ — **TIAA**

*Source: ticketmaster-first-call.md confirms — "Teams have autonomy → zoo of systems"*

### Theme 3: Knowledge Bottlenecks & Hero Culture
Ticketmaster named this explicitly: a "Resilience Analysis" team that acts as a human knowledge base — not scalable, not sustainable. Same pattern as HSBC and ADT.

> _"The key between these people and your production is fragmented knowledge that usually lies in meetings, in messaging, but also in runbooks that are not either present or always up to date."_ — **HSBC**

> _"With each new feature everything gets more complex and has more failure modes and it's rapidly becoming more than any individual person can easily keep a mental model of."_ — **Wayne Hill, SRE Manager, ADT**

> _"Nice. This is super helpful because we spend so much time building them [runbooks] and then they are not in the eye."_ — **Saasha Mor, SRE, Adobe (S3 POC)**

*Source: ticketmaster-first-call.md — "Heavy reliance on individuals. Not scalable. Desire for automation or augmentation."*

### Theme 4: Alert Fatigue — The Silent Reliability Tax
Ticketmaster: fully analyzing alerts would take an entire workday, so engineers only respond to critical ones. DoorDash POC shows this is also a retention risk once onboarded.

> _"I'm getting a lot of comments around brevity missing... people are just starting to ignore Resolve in some cases, which is kind of tough to see."_ — **Alex Danilychev, DoorDash SRE (S3 POC)**

> _"I myself have found it to be like a little information overload sometimes."_ — **Arin Champati, DoorDash**

*Source: ticketmaster-first-call.md — "High alert volume. Fully analyzing alerts would take an entire workday. Leads to alert fatigue, ignored alerts unless critical."*

### Theme 5: Scaling Ops Without Scaling Headcount
Every engineering leader is being asked to do more with the same (or smaller) team. Ticketmaster's "hero culture" and "constant firefighting" is the same pressure ADT and McKinsey described.

> _"Our system is probably gonna double over the course of the year if things go well, but our SRE team is not going to double in size and we're not gonna be able to afford to."_ — **Alexander Crettenand, Head of Software Engineering, ADT**

> _"Our teams are constantly being asked to do more with less."_ — **Krinal Manakiwala, McKinsey**

*Source: ticketmaster-first-call.md — "Unsustainable hero culture. Constant firefighting."*

### Theme 6: The "Aha Moment" — Autonomous Investigation Demo Converts Deals
Every deal that accelerated to S3+ shared one inflection point: a live demo connecting disparate signals autonomously.

> _"So it is kind of like that human replacing that human reviewer within like the observability process."_ — **Carla Hindley, Chief Data & Analytics Office, LBG**

> _"Aja had been beating his head against a wall all day on an issue. He was debugging, couldn't solve it. And after sitting down with Resolve for a bit, he was able to come to root cause using the tool."_ — **Internal Resolve sync, Adobe POC (S3)**

> _"Root cause found correctly. Nice."_ — **Adobe POC participant**

### Theme 7: "Build vs. Buy" Is the #1 Deal Blocker at S1–S2
Every large enterprise asked this. The competitive doc now provides hard numbers: 10–15 engineers, $10M+, 18–24 months to build comparable in-house. These need to become standard talk tracks.

> _"What do you do in that environment that we wouldn't be able to do ourselves? Or our own agents."_ — **Petek Ergul, HSBC**

> _"Because like, what is gonna be the difference between me asking Cloud Code to connect to my GCP client and figure this out versus using your service?"_ — **Mayank Agarwal, ADT**

---

## Pain Point Inventory
*(Ranked by frequency across all sources)*

| # | Pain | Sources | Best Verbatim |
|---|------|---------|---------------|
| 1 | High MTTR / customers find issues before you do | LBG, HSBC, Block, TIAA, Ticketmaster | "Customers act as canaries so they find the problem before we do." — LBG |
| 2 | Fragmented tooling, no end-to-end picture | TIAA, LBG, HSBC, ADT, Ticketmaster | "We have Dynatrace in some places, SignalFx in some places, nothing in others." — TIAA |
| 3 | Alert fatigue — engineers only respond to critical alerts | DoorDash, Ticketmaster, LBG | "Fully analyzing alerts would take an entire workday." — Ticketmaster |
| 4 | Overcrowded bridge calls with unnecessary engineers | LBG, HSBC, TIAA | "Our incidents have 20+ engineers on a single bridge." — LBG |
| 5 | Knowledge locked in senior engineers / tribal knowledge | HSBC, ADT, Adobe, Ticketmaster | "Fragmented knowledge that usually lies in meetings, in messaging, but also in runbooks." — HSBC |
| 6 | Scaling SRE ops without scaling headcount | ADT, McKinsey, DoorDash, Ticketmaster | "Our SRE team is not going to double in size and we're not gonna be able to afford to." — ADT |
| 7 | No root cause — know *what* broke, not *why* | TIAA, LBG, PicPay | "We know what's happening, what is broken, but we do not know why." — TIAA |
| 8 | Hero culture / unsustainable on-call burden | Ticketmaster, ADT | "Only respond to major incidents. Unsustainable hero culture. Constant firefighting." — Ticketmaster |
| 9 | Cold start problem for on-call engineers | Ticketmaster, ADT, HSBC | "On-call engineers often don't know where to begin. Face multiple simultaneous symptoms." — Ticketmaster |
| 10 | Ownership gaps, patchwork codebases | Invisible | "My biggest frustration is lack of clear ownership on a lot of these areas." — Invisible |

---

## Jobs To Be Done

1. **Find root cause before the CEO calls** — "Stop being surprised by outages my own customers found first."
2. **Clear the bridge call faster** — "Get the 15 engineers who aren't relevant off the call in under 20 minutes."
3. **Scale incident response without hiring** — "Handle 2x the system complexity without 2x the SRE team."
4. **Get new engineers on-call-ready in weeks, not months** — "Stop depending on 2 people who know everything."
5. **Get one coherent picture across fragmented tools** — "Stop context-switching between Splunk, Dynatrace, and Slack to piece together what happened."
6. **Eliminate hero culture** — "Stop having incidents that only one person can solve."
7. **Cut through alert noise to know what actually matters** — "Stop dedicating an entire workday to triaging alerts."
8. **Justify AI investment internally** — "Bring the CFO/board something with a clear ROI number, not a vibe."

---

## Competitive Landscape Signals

| Competitor / Alternative | What Prospects Said | Internal Positioning | Threat Level |
|---|---|---|---|
| **Splunk** | "Now Splunk is doing things you guys are doing." — HSBC | AI is bolt-on, restricted to Splunk data, no cross-stack reasoning | HIGH — entrenched incumbent expanding into RCA |
| **Datadog Bits AI** | Named as point-solution baseline | SaaS-only, limited to Datadog telemetry, per-investigation pricing unpredictable | HIGH — same data silo problem |
| **Dynatrace Davis** | Prospects expect proactive anomaly detection from Dynatrace | Agentic remediation in preview, limited to Dynatrace-ingested data | HIGH — the "proactive" gap exploitable |
| **PagerDuty** | Used at Ticketmaster (FireHydrant too) | Routing only, no logs/metrics/infra access, no root cause | MEDIUM — incumbent in alert layer, not a direct competitor |
| **ServiceNow** | "Must have" at TIAA (marketplace requirement) | CMDB goes stale, no autonomous investigation, 18+ months to AI autonomy | HIGH (FSI) — deal blocker AND indirect competitor |
| **Moogsoft** | "You don't have a Moogsoft connector." — TIAA | Not mentioned in competitive doc — gap | HIGH (FSI) — deal blocker |
| **Traversal, Deductive, Cleric** | Not named by prospects directly | Resolve: >$150M vs. less-funded, production since 2024 vs. 2025 launches, limited cross-stack depth | MEDIUM — emerging category competitors |
| **Build-Your-Own / Internal AI** | "Sometimes it gets better answers than Resolve." (PicPay). "We usually build things in house." (HSBC) | 10–15 engineers, $10M+, 18–24 months; fragile; no shared memory | VERY HIGH at eng-heavy enterprises |
| **Coding agents (Cursor, Claude Code)** | "What's the difference vs. asking Claude Code?" — ADT | Resolve: non-deterministic production troubleshooting vs. deterministic coding; different problem space | MEDIUM — strategic confusion, not active competition |

---

## Messaging Gaps (Preliminary)

1. **"Build vs. buy" needs hard numbers, not concepts.** Competitive doc now provides: 10–15 engineers, $10M+, 18–24 months. These need to be in every S1 talk track. Current answer is still hand-wavy in calls.

2. **Proactive vs. reactive positioning is unresolved.** Dynatrace/Datadog prospects expect proactive anomaly detection. "Triggered only, by choice" answer loses credibility without a sharp "why reactive is better" or explicit segmentation ("if you need proactive, Dynatrace is your tool — we solve what they can't").

3. **Alert fatigue is an underused entry point.** Ticketmaster led with alert volume as the primary pain — Resolve can speak to this but rarely does proactively. "What if every alert worth investigating was already investigated before you woke up?" is an untapped angle.

4. **Change detection gap is a deal staller at enterprise.** TIAA: "70% of your changes aren't covered." No roadmap story for non-software change (network, hardware, IAM, security config).

5. **ServiceNow marketplace absence is a credibility/compliance issue at FSI** — not just a technical gap. Needs to be addressed in pitch or have a clear "on roadmap, here's the timeline" answer.

6. **Pricing is opaque to enterprise procurement.** Adobe: "Very atypical for us." Need a "1 credit = X human engineer hours" translation that survives procurement scrutiny.

7. **Agent controllability is a retention risk for power users.** Block/Square's top SRE: "If you could just control the system prompt yourself... holy crap." Without tenant-level configurability, technically sophisticated customers compare Resolve unfavorably to internal tools.

8. **Database RCA is a known gap — and cost us a deal.** PicPay lost specifically because Resolve couldn't root-cause database issues. No message around where Resolve does/doesn't play on DB observability.

9. **ICP definition mismatch.** Real buyers in calls: Head of SRE, Principal SRE, VP Platform Engineering. Exec champion: CTO, Group Head of Data Science. Current competitive doc and example positioning don't reflect this split.

10. **"Hero culture" and "cold start problem" are resonant frames not yet in messaging.** Ticketmaster named both explicitly. These are human, emotional narratives that go beyond "reduce MTTR."

---

## Raw Evidence Bank

**On the bridge call / MTTR crisis:**
> _"MTTR is high — meantime to resolution takes us a long time. Customers act as canaries so they find the problem before we do. Our incidents have 20+ engineers on a single bridge."_ — Anestis Samaras, Group Head of Data Science, LBG (attention-calls-pmm-analysis-s1-s4.md)

> _"MTTR is high, customers are your canaries. So they report issues before you find them. And you have massive bridges with 20+ engineers on them."_ — HSBC CTO/Service Management (S2 demo) (attention-calls-pmm-analysis-s1-s4.md)

> _"Not getting a result in 30 minutes is like holy crap. Usually the whole thing will have been resolved in some short period of time, right? Like 15... something minutes maybe 20."_ — Brandon Zimmerman, Senior SRE, Block/Square (S3 POC) (attention-calls-pmm-analysis-s1-s4.md)

**On alert fatigue:**
> _"Many teams experience high alert volume. Fully analyzing alerts would take an entire workday. Leads to: Alert fatigue. Ignored alerts unless critical."_ — Yevhen Zavhorodnii, Principal SRE, Ticketmaster (ticketmaster-first-call.md)

> _"I'm getting a lot of comments around brevity missing... people are just starting to ignore Resolve in some cases, which is kind of tough to see."_ — Alex Danilychev, DoorDash SRE (S3 POC) (attention-calls-pmm-analysis-s1-s4.md)

**On fragmented tooling:**
> _"Our current environment is quite fragmented. We have different tools. There are some tools that don't have even basic observability at all. Some places we have Dynatrace, some places SignalFx, some places nothing."_ — Jay Rudrachar, TIAA (attention-calls-pmm-analysis-s1-s4.md)

> _"The number biggest problem that we have is each team sort of understands what the challenges are, but we don't have the end-to-end picture."_ — TIAA Operations leader (attention-calls-pmm-analysis-s1-s4.md)

> _"What we don't have is a mature resolve capability where we know what's happening, what is broken, but we do not know why and how to go about it. That's where we spend the majority of time."_ — TIAA (attention-calls-pmm-analysis-s1-s4.md)

**On hero culture / knowledge bottlenecks:**
> _"[Resilience Analysis team] Acts as incident coordinators. Serves as a human knowledge base. Issues: Heavy reliance on individuals. Not scalable. Desire for automation or augmentation."_ — Ticketmaster (ticketmaster-first-call.md)

> _"With each new feature everything gets more complex and has more failure modes and it's rapidly becoming more than any individual person can easily keep a mental model of."_ — Wayne Hill, SRE Manager, ADT (attention-calls-pmm-analysis-s1-s4.md)

> _"The key between these people and your production is fragmented knowledge that usually lies in meetings, in messaging, but also in runbooks that are not either present or always up to date."_ — HSBC (attention-calls-pmm-analysis-s1-s4.md)

**On the cold start / on-call pain:**
> _"On-call engineers often don't know where to begin. Face multiple simultaneous symptoms. Results in: Slow MTTR. Escalation to multiple teams."_ — Ticketmaster (ticketmaster-first-call.md)

**On scaling without headcount:**
> _"Our system is probably gonna double over the course of the year if things go well, but our SRE team is not going to double in size and we're not gonna be able to afford to."_ — Alexander Crettenand, Head of Software Engineering, ADT (attention-calls-pmm-analysis-s1-s4.md)

> _"Our teams are constantly being asked to do more with less."_ — Krinal Manakiwala, McKinsey (attention-calls-pmm-analysis-s1-s4.md)

**On tribal knowledge / runbooks:**
> _"Nice. This is super helpful because we spend so much time building them [runbooks] and then they are not in the eye. So that's amazing."_ — Saasha Mor, SRE, Adobe (S3 POC) (attention-calls-pmm-analysis-s1-s4.md)

**On the demo "aha moment":**
> _"So it is kind of like that human replacing that human reviewer within like the observability process."_ — Carla Hindley, Chief Data & Analytics Office, LBG (attention-calls-pmm-analysis-s1-s4.md)

> _"Aja had been beating his head against a wall all day on an issue. He was debugging, couldn't solve it. And after sitting down with Resolve for a bit, he was able to come to root cause using the tool. So that's pretty cool."_ — Internal Resolve sync, Adobe POC (S3) (attention-calls-pmm-analysis-s1-s4.md)

> _"Root cause found correctly. Nice."_ — Adobe POC participant (attention-calls-pmm-analysis-s1-s4.md)

**On the "build vs. buy" objection:**
> _"What do you do in that environment that we wouldn't be able to do ourselves? Or our own agents."_ — Petek Ergul, Service Management Lead, HSBC (attention-calls-pmm-analysis-s1-s4.md)

> _"Because like, what is gonna be the difference between me asking Cloud Code to connect to my GCP client and figure this out versus using your service?"_ — Mayank Agarwal, ADT (attention-calls-pmm-analysis-s1-s4.md)

*Internal answer (competition.md): "Requires 10–15 engineers, $10M+, 18–24 months. Systems degrade with team changes. No shared memory or learning."*

**On "no new system to learn" / Slack-native:**
> _"Resolve really helps because it doesn't have a single source of truth. It operates within the tools that you have and the environment that you have."_ — TIAA call (attention-calls-pmm-analysis-s1-s4.md)

**On day-one value:**
> _"If this is your bread and butter, that's what it is. Just implement it. Put your system integrations in. You should be able to show value in a week."_ — Jay Rudrachar, Observability Lead, TIAA (attention-calls-pmm-analysis-s1-s4.md)

**On the postmortem / cited RCA report:**
> _"The thing that this tool does really well is it basically constructs an entire postmortem... it has a very cited postmortem where it's like, multiple of us have looked at it and we're like, geez, it has a lot of citations, it has a lot of links to all the stuff."_ — Brandon Zimmerman, Block/Square (S3 POC) (attention-calls-pmm-analysis-s1-s4.md)

**On pricing opacity:**
> _"It's a very opaque pricing model compared to what we are accustomed to seeing. There's no opportunity to separate that into a platform cost and a purchasing of tokens cost."_ — Adobe procurement (S4) (attention-calls-pmm-analysis-s1-s4.md)

> _"We are accustomed to receiving transparency on what a credit is defined as. That is very vague here — it's defined by work stream units."_ — Adobe procurement (attention-calls-pmm-analysis-s1-s4.md)

**On agent controllability:**
> _"If you could just control the system prompt yourself... holy crap, then it will probably start performing on all the ones that BuilderBot performs better on."_ — Brandon Zimmerman, Block/Square (attention-calls-pmm-analysis-s1-s4.md)

**On deal loss (PicPay):**
> _"It never gave us a root cause related to database... The max that we had was like, oh, you have slow queries investigate that, but this is what we both have."_ — Daniel Reis, PicPay (attention-calls-pmm-analysis-s1-s4.md)

**On unnecessary human reviewer (differentiated framing):**
> _"It's replacing also the unnecessary human reviewer. Very common in banks — you have latency, you call up network, 70% of the time it's not network's fault, but you've still engaged one to two to three engineers from network."_ — Vasi Karkantzos, Resolve (confirmed by LBG prospect) (attention-calls-pmm-analysis-s1-s4.md)

**On change detection gap:**
> _"What I am seeing in your roadmap is all software change — GitHub, GitLab, Kubernetes, that's it. That is only 30% of our change. 70% you're not even covered here."_ — Jay Rudrachar, TIAA (attention-calls-pmm-analysis-s1-s4.md)

**Proof points (from competition.md):**
- Coinbase: 72% faster investigations
- DoorDash: 87% faster investigations  
- Zscaler: 30% fewer engineers per incident
