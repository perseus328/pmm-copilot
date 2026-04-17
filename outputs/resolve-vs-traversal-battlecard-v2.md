# Internal

# Resolve AI vs. Traversal

NOT READY FOR USE — GOING THROUGH REVIEWS

**Internal battlecard. Confidential.**

*For AE, SE, and Engineering use only. Not for external distribution. Version 2.0, April 2026*

---

## **Quick reference**

**You may see Traversal:** Enterprise FSI accounts, large-scale infrastructure environments, security-conscious regulated industries, and any account where someone has read their Sequoia- or Kleiner Perkins-backed press. They are increasingly aggressive in the market following their Amex Ventures investment (March 2026), and a significant sales team hire from Cribl.

**One-line response when Traversal comes up:** "Traversal is an AI SRE built for automated incident conclusions. We are AI for prod, built for autonomous actions and how engineers actually work through problems. The difference shows up the moment an investigation comes back incomplete and the engineer needs to go deeper."

**Do not dismiss them.** Their causal ML research is real, their enterprise traction is growing, and their founding team is credible. Reps who dismiss Traversal lose credibility with technical buyers. Acknowledge their strengths, then redirect.

---

## **Company snapshot**

|  | Resolve AI | Traversal |
| ----- | ----- | ----- |
| **Founded** | 2024 | 2024 |
| **HQ** | San Francisco | New York |
| **Funding** | $160M+, Lightspeed and Greylock, $1B valuation | $48M, Sequoia and Kleiner Perkins, plus Amex Ventures (March 2026) |
| **Team** | 130+ total, 70-person engineering and research team | ~40 to 50 total (LinkedIn numbers) |
| **Founding team** | Spiros Xanthos and Mayank Agarwal, co-creators of OpenTelemetry and former leaders of Splunk Observability | Anish Agarwal (CEO) and three MIT researchers with PhDs in causal ML and reinforcement learning, one co-founder from Citadel Securities |
| **Research depth** | Google Deep Research, Meta Superintelligence Labs | MIT and Columbia PhDs, causal ML focus |
| **Key customers** | Coinbase, DoorDash, Zscaler, Salesforce, MongoDB, MSCI, Millennium, Toast, Guidewire, Cisco | American Express, Pepsi, DigitalOcean, Cloudways, Eventbrite |

---

## **Where we win**

### **1. Multi-turn interactive investigation**

This is the single most important differentiator and the one most grounded in real evidence. Traversal's documented workflow is primarily investigation-first and automated. Their docs do note that investigations can be continued with follow-ups in Slack — so do not claim they have zero follow-up capability. The meaningful distinction is depth and statefulness.

Resolve's investigation model keeps full context within and across sessions. Engineers can ask follow-up questions that change the direction of an investigation, add context that wasn't available at the start, and pivot to different modes — all in a single continuous session. This is not the same as posting a follow-up message in a Slack thread after an automated summary has been delivered. It is a stateful, conversational debugging loop where the AI is holding the full investigation context and adapting in real time.

In competitive evaluations where Traversal was also in the room, the ability to go deeper mid-stream — rather than receive one finding and continue in a different channel — has repeatedly been the stated deciding factor at enterprise accounts.

**SE note:** Build your demo around this. Show a multi-turn investigation where the second question materially changes the direction. Ask the prospect: "When an investigation comes back and the answer feels incomplete, what does your team do?" Let them answer before you show the capability.

### **2. Scope: AI for prod vs. AI SRE**

Traversal's CEO has stated publicly that incidents are where their technical moat is strongest. Their docs describe a somewhat broader scope — alert triage, knowledge capture, proactive system understanding — but incident investigation and automated RCA remain the primary publicly documented use case and the center of their market narrative.

Resolve operates across alerts, incidents, and production debugging today, with automated remediation, proactive optimization, operational reporting, and enhanced teachability in active development.

This matters in deals where the buyer is an engineering leader rather than a VP of SRE. Developers, platform engineers, and anyone who touches production daily gets more value from Resolve's broader platform scope.

**How to use this:** Don't overstate the "incidents-only" claim. Say instead: "Traversal is strongest publicly around incident investigation and RCA. Resolve covers that and is also the platform your developers and platform engineers use for daily production work."

### **3. Code-level understanding**

Traversal uses code and deployment data as part of its reasoning — their docs mention mining telemetry and code to build their system world model, and GitHub is a supported integration. Code is not absent from their model.

The differentiation is centrality. Resolve makes code-aware investigation and developer workflow front and center: correlating code changes to production behavior, generating git-ready fixes, creating PRs, and providing production context to developers as they write code. When the root cause is a deployment or a code change, Resolve traces it end-to-end and brings the developer into the resolution loop.

**Suggested language:** "Traversal uses code and deployment data as an input. Resolve makes that connection a first-class output — the code path, the commit, the PR — so the person who wrote it can fix it."

### **4. Enterprise customer breadth**

Traversal's customer base is concentrated in FSI and infrastructure. Resolve has published proof points across fintech (Coinbase, MSCI, Millennium, Upgrade), security (Zscaler), enterprise SaaS (Salesforce, Guidewire), databases (MongoDB), and consumer scale (DoorDash, Toast). For accounts outside FSI, Resolve's proof points are more relevant and more varied.

### **5. Team depth across both domains**

Traversal's team is strong on AI research but light on observability domain experience. Resolve's founding team co-created OpenTelemetry and ran Splunk Observability, combined with engineering leaders from Google Deep Research and Meta Superintelligence Labs. For technical buyers who care about whether the team understands production systems — not just models — this is a real differentiator.

### **6. Governance and compliance — a documentation visibility gap, not a product absence**

Traversal's docs do publicly state that customer data is protected through strict isolation, access controls, and privacy safeguards. They also emphasize that their product is read-only by design, with no write privileges to data stores or code. Do not claim they have no security controls — that is incorrect and will be immediately challenged.

What their public documentation does not prominently feature is specific tooling around RBAC, audit trails, and multi-tenant isolation. Those controls are essential in regulated environments where "we have access controls" is not the same as "you can scope which teams see which services" or "you have a full audit log of every query Resolve ran during this incident."

Resolve has team-scoped RBAC, full audit trails for every investigation and action, multi-tenant isolation, and built-in SOC 2, HIPAA, and PCI DSS compliance. Lead with what you have, not with what you think they lack.

**Suggested language:** "Traversal emphasizes privacy safeguards and read-only access — which is genuinely good for security posture. What their docs don't detail publicly is granular RBAC and audit trails at the level regulated environments require. We document and deliver both."

---

## **Where Traversal is stronger**

### **1. Deployment model**

**Real example to keep in mind internally:** The AMEX situation is more nuanced than a clean Traversal win. Resolve ran a successful POC at AMEX with genuine adoption, positive user feedback, and momentum toward a paid engagement. The process stalled due to a major org restructure: Nidal moved roles, two new VPs were being hired, and budget ownership shifted to a new Tooling org that had not yet been staffed. Both Resolve and Traversal were paused for the same structural reason. Traversal's Amex Ventures investment and deployment announcement came after that restructure, not as a result of a head-to-head product evaluation. Their advantage was on-prem clearance speed and a bespoke UI tailored to AMEX's environment. Do not represent AMEX as a Traversal competitive win on product merit. It was not.

### **2. Read-only, agentless architecture — a genuine security story**

Traversal's docs explicitly state:
- "Read-only by design"
- "No agents to deploy"
- "No write privileges to your data stores or code"
- Only minimal Slack messaging scope for posting investigation results back into channels

This is a genuinely strong security posture and should be acknowledged as such. In regulated environments where infosec teams are the primary gating function, this is a meaningful advantage in the approval process. Don't fight it — qualify around it: "Does security clearance speed matter more to you than what the product does once deployed?"

### **3. Bring your own model (new flag for engineering)**

Traversal recently introduced a bring-your-own-model configuration, allowing customers to substitute their own approved LLM. This is appealing in regulated industries where organizations have already approved specific models internally.

**The landmine:** BYOM introduces real questions about consistency and accuracy that Traversal does not answer publicly. Their Causal Search Engine and Production World Model are tuned against specific model behavior. Swapping in an untested model changes how the system reasons, and there are no published accuracy benchmarks for non-default configurations.

**How to handle it:** "Traversal's BYOM option sounds flexible, but their 82% RCA accuracy claim is based on their default model configuration. There are no published benchmarks for how accuracy changes when you substitute a different model. Resolve employs a multi-model approach from open source and custom models, continuously evaluated against production deployments. You get flexibility without sacrificing the accuracy guarantees."

**Flag for engineering:** Traversal's BYOM announcement is recent and worth monitoring. If they publish accuracy benchmarks for non-default configurations, that changes the competitive calculus.

### **4. Causal ML research pedigree**

Traversal's founders are genuine researchers with published work in causal machine learning. Their "correlation vs. causation" narrative resonates strongly with technical buyers who understand the limitations of alert correlation tools. Anish Agarwal is a Columbia professor with academic credibility.

**How to handle it:** Do not dismiss it. "Traversal's causal ML research is real, and it is a genuine technical contribution. The question is whether the research foundation translates to better outcomes in your environment. Resolve's research team includes engineering leaders from Google Deep Research and Meta Superintelligence Labs who have worked on frontier AI systems that power production-grade reasoning at scale. Academic research and applied production AI research are different bets."

### **5. Alert intelligence at petabyte scale**

Traversal's Alert Intelligence product is purpose-built for very high alert volumes: 15,000+ alerts per day, petabyte-scale telemetry, and continuous triage. Their parallel query architecture reflects a real investment in breadth of coverage.

**How to handle it:** Qualify first. "What is your actual alert volume, and how many of those become real incidents?" Most accounts will find that alert volume is not their primary constraint. If an account genuinely has 10,000+ alerts per day and wants fully automated triage with no human involvement, Traversal may be a better fit for that specific workflow. Do not lose a deal on a use case the prospect does not actually have.

### **6. Forward-deployed engineering at key accounts**

Traversal embeds engineers on-site at major accounts, effectively acting as contractors within the customer environment. This creates deep relationships, faster iteration, and custom UI development that wins deals in the short term.

**How to handle it:** "Traversal's forward deployment model creates a tight feedback loop early on. It also means their product roadmap gets shaped by one customer's requirements at a time, and the custom UI they build for one account does not benefit others. Resolve's platform approach means every customer benefits from a shared product roadmap, and our customer success and SE team provides the same depth of support without requiring on-site engineers."

---

## **Objection handling quick reference**

| Objection | Response |
| ----- | ----- |
| "Traversal has causal ML, you just use LLMs" | "Resolve's multi-agent architecture distributes reasoning across specialized agents with independent cross-checks. The outcome is more robust than a single causal reasoning path, especially when signals are partial or contradictory." |
| "Traversal runs 10,000 parallel queries" | "Parallel breadth and contextual depth are different approaches to the same problem. For complex novel incidents, holding full system context in a single reasoning session outperforms fragmenting it across 10,000 narrow queries." |
| "We want fully autonomous, no human in the loop" | "Resolve supports full autonomous investigation. The difference is that Resolve also lets engineers collaborate on that investigation when needed. You are not choosing between autonomous and interactive; you get both." |
| "Traversal is backed by Sequoia and KP" | "Resolve is backed by Lightspeed and Greylock at a $1B valuation with $160M raised, more than three times Traversal's total funding, with both companies starting around the same time in 2024. The investor quality question cuts both ways." |
| "Traversal on-prem clears security faster" | "That is true in some regulated environments. The question is whether security clearance speed is the primary criteria, or whether what the product does once deployed matters more." |
| "Traversal has BYOM so we can use our approved model" | "BYOM sounds flexible but Traversal has not published accuracy benchmarks for non-default model configurations. Their 82% RCA claim is based on their default setup. Ask them what happens to accuracy when you swap the model." |
| "Traversal supports follow-ups in Slack" | "Their docs do mention Slack follow-ups. The difference is a stateful conversational debugging loop — where the AI is holding full context and adapting in real time — versus following up on an automated summary that has already concluded. In complex incidents, those are very different experiences." |

---

## **Discovery questions to surface Traversal gaps**

Use these before Traversal comes up, not after. If you have already established the answers, the competitive comparison lands on your terms.

- "When an investigation comes back and the answer feels incomplete, what do you do next?"
- "How often does root cause cross service or team boundaries in your environment?"
- "How much time does your team spend on post-mortems, handovers, and SLO reporting outside of active incidents?"
- "Does your security policy require data to stay within your own infrastructure, or is SaaS acceptable?"
- "Have you approved a specific LLM vendor internally, and does that affect your evaluation?"
- "What does your alert volume look like, and how many of those become real incidents per month?"
- "When you get a root cause finding from a tool, do your engineers typically accept it or do they want to interrogate it?"

---

## **Watch list: Traversal recent signals**

**Amex Ventures investment (March 2026):** Traversal now has a direct financial and commercial tie to American Express. That account is locked in. More importantly, it gives them a flagship FSI reference that will accelerate conversations at Citi, JPMorgan, Barclays, and other major banks. Expect their FSI pipeline to grow materially in H1 2026.

**Cribl sales team hire:** Traversal recently hired significant sales talent from Cribl, including a sales leader and multiple enterprise AEs and SE leaders. Their GTM will become more aggressive. Deals that were slow-moving will start to accelerate.

**BYOM announcement:** The bring-your-own-model configuration is new and signals that Traversal is responding to enterprise objections about model approval. Monitor this closely. If they publish accuracy benchmarks for non-default configurations it becomes a stronger story. For now, probe the consistency question.

---

## **For engineering: technical landmines to flag**

**Traversal's Production World Model architecture — probe freshness, don't assert lag:**
Traversal re-indexes customer telemetry into their proprietary world model using compression and re-ranking. Their architecture is well-documented in this respect. What is worth probing in technical evaluations is freshness: how quickly does the Production World Model reflect new system state after a configuration change, deployment, or novel failure mode during a fast-moving incident? This is not a documented limitation — it is a discovery question worth asking. "What is the lag between a change in your environment and the Production World Model reflecting it?"

**BYOM accuracy consistency:** BYOM with no published accuracy benchmarks is a real engineering concern. The causal ML reasoning is tuned to specific model behavior. Substituting an untested model introduces unknown behavior in a system where accuracy directly affects production decisions.

**Multi-agent vs. causal search — our inference, not their documented limitation:**
Traversal's docs emphasize causal search and high query breadth: approximately 10,000 investigative queries where traditional tools run around 100. From a competitive standpoint, Resolve's position is that multi-agent cross-checking — distributing reasoning across independent specialist agents — offers a different architectural tradeoff when production signals are incomplete or contradictory. One agent's conclusion is checked against another's. This is our competitive inference from their architecture, not a documented failure mode. Present it that way: "Their causal search approach concentrates reasoning in one path. We distribute it across independent agents. In noisy or ambiguous environments, we believe that's the more resilient design."

**Parallel queries vs. context depth:** Traversal's 10,000 parallel query claim reflects breadth of coverage. For incidents that require reasoning across the full system simultaneously, fragmenting the investigation into thousands of narrow queries loses the relational context that connects the pieces. Resolve's 1M context window means full investigation context — including code, infrastructure state, incident history, and telemetry — can be held in a single reasoning session.

*Internal use only. Do not share externally.*
*Owner: GTM / Product Marketing*
*Next review: Q2 2026*

---

# General Resolve vs. Traversal (External)

# **Resolve AI vs. Traversal**

NOT READY FOR USE — GOING THROUGH REVIEWS

## **AI for Production vs. AI SRE**

Both Resolve AI and Traversal are serious AI products for production operations. Traversal is an AI SRE tool strongest publicly around automated incident investigation and RCA, with documented capabilities across alert triage, knowledge capture, and proactive system understanding. Resolve AI is an AI platform for running production: covering autonomous alert investigations, collaborative incident remediation, interactive debugging, and daily production operations, with an engineering and research team and customer base that reflects that broader ambition.

The practical difference: Resolve AI is designed to help engineers work through production problems autonomously and collaboratively. Traversal is optimized to produce conclusions.

|  | Resolve AI — Founded 2024 | Traversal — Founded 2024 |
| ----- | ----- | ----- |
| **Category** | AI for Prod | AI SRE |
| **Core focus** | Automated alert triage and investigations, collaborative incident remediation, interactive debugging, and daily production operations | Automated incident investigation and alert triage, with documented scope across knowledge capture and proactive monitoring |
| **Investigation model** | Multi-turn stateful investigation: follow-up questions, mid-stream pivots, multiple modes — full context maintained throughout | Automated investigation with results delivered in Slack with follow-up capability; optimized for automated conclusions |
| **Data approach** | Live context graph built directly from your existing tools, no separate data layer | Proprietary Production World Model, telemetry re-indexed into a separate vendor-managed layer |
| **Architecture** | Multi-agent system with specialized agents across logs, metrics, traces, infrastructure, code, and deployment history | Centralized Causal Search Engine reasoning over a single indexed model |
| **Transparency** | Full evidence citations linked directly to your own tools, fully auditable | Confidence score with root cause finding |
| **Knowledge capture** | Resolve.md and Skills, version-controlled, engineer-editable, compounds over time | Static Knowledge Bank, upload runbooks and documents |
| **Governance** | RBAC, audit trails, multi-tenant isolation, SOC 2, HIPAA, and PCI-DSS compliant | Read-only access, privacy safeguards, strict isolation, and access controls documented; granular RBAC and audit trail documentation not prominent in public materials reviewed |
| **Team size** | 130+ employees, 70-person engineering and research team | ~40 to 50 people total |
| **Funding** | $150M+, Lightspeed and Greylock, $1B valuation (at Series A) | $48M, Sequoia and Kleiner Perkins (at Series A) |

### **1. Live context graph built from your existing tools**

Resolve builds a dynamic context graph across your infrastructure, services, telemetry, and code, using the systems your engineers already use and trust.

- Connects directly to existing tools: Grafana, Datadog, Kubernetes, GitHub, and others
- Investigates against live systems in real time
- Does not require teams to operate a separate investigation data layer
- Your data stays in your tools, with no vendor-managed representation of your environment

Engineers investigate against the same systems they rely on every day, keeping findings grounded and immediately verifiable.

### **2. Multi-agent system: a jury of experts, not a single reasoning path**

Resolve uses a multi-agent architecture where specialized agents handle different aspects of an investigation — logs, metrics, traces, infrastructure state, dashboards, alerts, code, and deployment history. A planning layer coordinates the investigation strategy.

When agents converge on the same root cause from different evidence sources, confidence increases. When they diverge, the investigation continues rather than prematurely settling on a single explanation.

This distributes reasoning across independent perspectives rather than concentrating it in one path. In environments where production signals are noisy, incomplete, or contradictory, we believe this is the more resilient architectural choice — though both approaches reflect genuine engineering investment.

### **3. Tool-native investigations, not black-box analysis**

Resolve investigates how engineers work, executing real queries against live systems rather than abstracting everything behind a proprietary analysis layer.

- Queries dashboards, searches logs, examines traces
- Checks infrastructure state and correlates deployments and code changes
- Every finding links directly to the underlying evidence in your own tools
- Investigations are fully transparent and auditable

For production incidents, that transparency is what makes AI output trustworthy enough to act on.

### **4. Stateful interactive investigation**

Resolve is designed for how engineers actually debug complex problems. Teams can:

- Start with autonomous RCA
- Ask follow-up questions and add context mid-investigation
- Pivot direction as new evidence surfaces
- Continue exploring across multiple modes: deep RCA, interactive chat, ticket-based investigation, and free-form exploration

Traversal supports follow-up in Slack after an automated investigation delivers its finding. What Resolve offers is meaningfully different: a stateful debugging loop where the full investigation context is maintained, the AI adapts to new direction in real time, and engineers can redirect at any moment without starting over. Complex incidents rarely follow a single clean path. In enterprise evaluations, this distinction has repeatedly been the deciding factor.

### **5. Self-service operational knowledge with Resolve.md and Skills**

Resolve gives teams a self-service way to encode how their production environment actually works.

- **Resolve.md** captures debugging heuristics, defines custom workflows, creates slash commands for common investigations, and codifies tribal knowledge in version-controlled form
- **Skills** let teams build specialized investigation capabilities tailored to their environment

This turns operational knowledge from something that lives in a senior engineer's head into a durable system asset that compounds over time — and persists as team composition changes.

### **6. Enterprise governance and access control**

Running AI in production at enterprise scale requires more than investigation accuracy. Traversal's docs are clear that their product is read-only by design, with privacy safeguards and strict isolation — that is a genuinely good foundation. What enterprise environments also require is granular controls: which team can see which service, a full audit trail of every query run during an incident, and isolation enforcement at the multi-tenant level.

Resolve AI is built with governance as a first-class capability:

- **Role-based access control** scopes investigations to the specific services and environments each team is authorized for
- **Data access boundaries** enforce existing organizational boundaries rather than creating new ones to manage
- **Audit trails** capture every investigation, every query, and every action taken — meeting SOC 2, HIPAA, and PCI-DSS requirements
- **Multi-tenant isolation** ensures investigations cannot surface data across tenant or team boundaries

Resolve leads with these explicitly because regulated environments require documentation, not just assurance.

### **Built at the intersection of frontier AI research and observability**

AI for production requires depth in two domains that rarely overlap: production systems at enterprise scale, and frontier AI research.

**Observability foundation:** Resolve AI was founded by Spiros Xanthos and Mayank Agarwal, co-creators of OpenTelemetry — now the second most active CNCF project after Kubernetes — and former leaders of Splunk Observability.

**Frontier AI research:** The engineering team brings deep expertise from Google Deep Research and Meta Superintelligence Labs, researchers who have worked at the frontier of what AI systems can reason over and act on in complex, real-world environments.

Production environments present a different class of problem than standard AI benchmarks: noisy telemetry, partial signals, distributed dependencies, and workflows where mistakes carry real consequences. Solving them requires both.

### **Proven with technical teams at scale**

Trusted by engineering organizations including Coinbase, DoorDash, Zscaler, Salesforce, MongoDB, Toast, and Guidewire.

- **73% reduction** in time spent on Sev2+ incidents at Coinbase
- **7-minute** average time to first hypothesis
- Deployed across complex multi-cluster Kubernetes environments processing billions of logs daily
- Enterprise security: SOC 2, HIPAA, and PCI-DSS compliant

### **Expanding beyond AI SRE**

Incident investigation is where AI for production begins, not where it ends. Resolve already operates across alerts, incidents, and production debugging. The platform is actively expanding across four adjacent outcome areas:

| Capability | What It Delivers |
| ----- | ----- |
| **Automated remediation** | Safely closes the loop between diagnosis and resolution |
| **Proactive optimization** | Surfaces reliability issues before they escalate |
| **Operational reporting** | Automates SLO reports, handovers, and production summaries |
| **Enhanced teachability** | Learns continuously from how engineers investigate and operate production |

### **When Resolve AI is the right fit**

- Engineers value stateful interactive investigation, not just one-pass automated RCA
- Incidents span services, infrastructure, and code boundaries
- Transparency and auditability during production incidents matter
- Investigations should be grounded in your existing observability stack
- Preserving operational knowledge across team changes is important
- You want a broader AI for production platform, not a narrower AI SRE tool

---

# Salesforce

# **Resolve AI vs. Traversal**

### **A Comparison for Engineering and SRE Teams**

Both Resolve AI and Traversal are serious AI products for production operations. Traversal is an AI SRE tool strongest publicly around automated incident investigation and RCA. Resolve AI is an AI platform for running production — covering autonomous alert investigations, collaborative incident remediation, interactive debugging, and daily production operations.

The practical difference: Resolve AI is designed to help engineers work through production problems autonomously and collaboratively. Traversal is optimized to produce conclusions.

|  | Resolve AI — Founded 2024 | Traversal — Founded 2024 |
| ----- | ----- | ----- |
| **Category** | AI for Prod | AI SRE |
| **Core focus** | Automated alert triage and investigations, collaborative incident remediation, interactive debugging, and daily production operations | Automated incident investigation and alert triage, with documented scope across knowledge capture and proactive monitoring |
| **Investigation model** | Stateful multi-turn investigation: follow-up questions, mid-stream pivots, multiple modes — full context maintained throughout | Automated investigation with Slack delivery and follow-up capability; optimized for automated conclusions |
| **Data approach** | Live context graph built directly from your existing tools, no separate data layer | Proprietary Production World Model, telemetry re-indexed into a vendor-managed layer |
| **Architecture** | Multi-agent system with specialized agents across logs, metrics, traces, infrastructure, code, and deployment history | Centralized Causal Search Engine reasoning over a single indexed model |
| **Transparency** | Full evidence citations linked directly to your own tools, fully auditable | Confidence score with root cause finding |
| **Knowledge capture** | Resolve.md and Skills, version-controlled, engineer-editable, compounds over time | Static Knowledge Bank, document upload |
| **Team size** | 130+ employees, 70-person engineering and research team with deep AI and observability expertise | ~40 to 50 people total |
| **Funding** | $150M+, Lightspeed and Greylock, $1B valuation (at Series A) | $48M, Sequoia and Kleiner Perkins (at Series A) |

### **How each product investigates**

This is the most consequential architectural difference for a complex environment like Salesforce.

**Resolve AI** investigates your live systems directly, using a multi-agent system that runs specialized agents across logs, metrics, traces, infrastructure state, code, and deployment history in parallel. A planning layer coordinates the investigation strategy, and engineers can:

- Start with autonomous RCA and ask follow-up questions
- Add context mid-investigation as new information surfaces
- Pivot direction without starting a new session
- Work across multiple modes in one platform: deep RCA, interactive chat, ticket-based investigation, and free-form exploration

**Traversal** runs an automated investigation against its Production World Model, with results delivered in Slack where follow-ups are possible. Their system is built for automated conclusions at scale. What is different from Resolve is the statefulness: Resolve maintains full investigation context throughout the debugging session, adapting in real time as engineers redirect. For production environments where incidents cross service boundaries, involve partial or contradictory signals, or require context that only emerges mid-investigation, the stateful model consistently outperforms single-shot automation.

### **Team-based governance and access control**

Running AI in production at enterprise scale requires controls that match how engineering organizations actually operate. Traversal's docs note that their product is read-only by design with privacy safeguards and strict isolation — a sound foundation. What enterprise environments also require is granular access controls and documented audit capability.

Resolve AI is built with governance as a first-class capability:

- **Role-based access control** scopes investigations to the specific services and environments each team is authorized for
- **Data access boundaries** enforce existing organizational boundaries rather than creating new ones to manage
- **Audit trails** capture every investigation, every query, and every action taken — meeting SOC 2, HIPAA, and PCI-DSS requirements
- **Multi-tenant isolation** ensures that in multi-product architectures, investigations are fully scoped and cannot surface data across tenant or team boundaries

This is particularly relevant for Salesforce, where multiple products, teams, and compliance requirements coexist in the same production environment. As AI systems take on more operational work, the controls around what they can see, what they can do, and who can direct them become as important as the quality of the investigation itself.

### **Research and team depth**

Both companies have genuine AI research credentials. The difference is in depth and domain.

**Resolve AI** combines 20+ years of observability domain expertise with frontier AI research:

- **Spiros Xanthos and Mayank Agarwal**, co-creators of OpenTelemetry and former leaders of Splunk Observability
- **Engineering leaders from Google Deep Research**, the team behind some of Google's most advanced AI reasoning systems
- **Engineering leaders from Meta Superintelligence Labs**, including Llama pre-training, data mix optimization, scaling laws, and synthetic data research across knowledge, code, and reasoning models

**Traversal** was founded by MIT and Columbia PhD researchers with backgrounds in causal machine learning. The founding team is academically strong, and their causal ML approach is a real technical contribution.

AI for production is not a pure research problem. It requires deep expertise in how production systems actually behave, combined with frontier AI research capability to reason reliably across them. Resolve is the only team in the space with both at depth.

### **Enterprise deployment at scale**

**Resolve AI** is deployed across a broader range of enterprise environments:

- Financial infrastructure: Coinbase, MSCI, Millennium, Upgrade
- Security and cloud: Zscaler, MongoDB
- Enterprise SaaS: Salesforce, Guidewire, Toast
- Consumer scale: DoorDash

**Traversal** is deployed at American Express, Pepsi, and DigitalOcean.

At Coinbase, Resolve reduced time spent on Sev2+ incidents by 73%, with an average time to first hypothesis of 7 minutes. Resolve AI operates across complex, multi-cluster Kubernetes environments, processing billions of logs daily, and is SOC 2, HIPAA, and PCI DSS compliant.

### **Why this matters for Salesforce**

Salesforce's production environment is multi-product, operates at significant scale, and involves complex service ownership across teams. The incidents that matter most are not clean single-service failures that automated one-shot RCA handles well. They are the ones that cross service boundaries, involve partial signals, and require an engineer to combine what the AI surfaces with context that only they hold.

That is exactly the scenario in which stateful interactive investigation with a live context graph outperforms automated conclusions delivered to a Slack thread. Traversal is a credible product for organizations optimizing for fully automated incident triage at scale. For an environment like Salesforce, Resolve AI is the stronger fit.

---

# Addepar

# **Resolve AI vs. Traversal**

### **For Addepar Engineering and SRE Leadership**

Both Resolve AI and Traversal are AI products for production operations. This document covers the meaningful differences in architecture, investigation model, integration maturity, and feature depth, so your team can make a confident decision without requiring a parallel POC.

The bottom line: Traversal is built for high-volume automated alert triage at petabyte scale. Addepar's stated use case is collaborative incident investigation in Slack channels, with engineers in the loop on real incidents. That is exactly what Resolve AI is designed for, and what it is already doing in your environment today.

|  | Resolve AI — Founded 2024 | Traversal — Founded 2024 |
| ----- | ----- | ----- |
| **Category** | AI for Prod | AI SRE |
| **Core use case** | Collaborative incident investigation, interactive debugging, and daily production operations | Automated alert triage and incident investigation, strongest publicly at high alert volume |
| **Investigation model** | Stateful multi-turn: engineers ask follow-up questions and add context mid-investigation with full context maintained | Automated investigation with Slack delivery and follow-up capability; optimized for automated conclusions |
| **Slack integration** | Native, bi-directional, investigations surface in incident channels with full thread context; engineers can direct investigation from Slack | Available, alert-triggered, with follow-up in Slack; primarily designed for automated finding delivery |
| **Data approach** | Live context graph from your existing tools, no separate data layer | Proprietary Production World Model, telemetry re-indexed into a vendor-managed layer |
| **Architecture** | Multi-agent system across logs, metrics, traces, infrastructure, code, and deployment history using a multi-model approach | Centralized Causal Search Engine over a single indexed model |
| **Transparency** | Full evidence citations linked to your own tools, fully auditable | Confidence score with root cause finding |
| **Knowledge capture** | Resolve.md and Skills, version-controlled, engineer-editable | Static Knowledge Bank, document upload |
| **Governance** | RBAC, audit trails, multi-tenant isolation, SOC 2, HIPAA, and PCI-DSS compliant | Read-only access, privacy safeguards, and access controls documented; granular RBAC and audit trail documentation not prominent in public materials reviewed |
| **Team size** | 130+ employees, 70-person engineering and research team | ~40 to 50 people total |
| **Funding** | $150M+, Lightspeed and Greylock, $1B valuation (at Series A) | $48M, Sequoia and Kleiner Perkins (at Series A) |

### **Why Traversal's core strength is not Addepar's problem**

Traversal's most-cited customer result is handling 15,000+ alerts per day at Pepsi with their Alert Intelligence product. Their marketing is built around automated triage at petabyte scale, with minimal human involvement.

Addepar's environment is different. Alert volume is not the constraint. Of roughly 4,500 alerts per month, approximately 15 become real incidents. The problem is not filtering noise at scale. It is getting the right context into incident channels fast, enabling engineers to investigate collaboratively, and reaching the root cause without hours of manual work across fragmented tools.

That is a collaborative investigation problem, not a bulk triage problem. Traversal's architecture is optimized for the latter. Resolve AI is built for the former.

Running a Traversal POC to evaluate a use case that their product is not primarily designed for introduces timeline risk, evaluation overhead, and internal distraction — for a question that Resolve's active deployment in your environment is already answering.

### **Integration depth and maturity**

Integration maturity is where the gap between the two products is most concrete.

**Resolve AI** integrates across the full production stack your engineers use today:

- Observability: Datadog, Grafana, New Relic, Splunk, Prometheus, Loki, and others
- Infrastructure: AWS (50+ services), Kubernetes, GCP, and Azure
- Code and CI/CD: GitHub, GitLab, Jenkins, and CircleCI
- Incident management: PagerDuty, ServiceNow, Jira, Linear, and OpsGenie
- Communication: Slack (native, bi-directional, full thread context) and Microsoft Teams
- Knowledge: Confluence, Notion, and Google Docs

Resolve's Slack integration is purpose-built for incident workflows. Engineers can @mention Resolve directly in incident channels, ask follow-up questions in thread, and continue the investigation interactively without leaving Slack. Context from the thread is carried into the investigation automatically.

**Traversal** also supports a broad integration set including Datadog, Grafana, Splunk, PagerDuty, ServiceNow, Jira, GitHub, Confluence, Notion, and Slack, among others. Their Slack integration delivers automated investigation findings into Slack and supports follow-up in thread. The meaningful difference is how engineers interact with that Slack integration: Traversal's workflow is optimized for receiving and reviewing automated findings; Resolve's is optimized for engineers directing the investigation from within the channel.

### **Feature gaps: what Traversal does not have**

Based on Traversal's published documentation and product positioning, the following capabilities are absent or not prominently featured:

**No stateful multi-turn debugging loop.** Traversal supports follow-up in Slack after an automated finding is delivered. What it does not offer is a stateful investigation session where the full context is maintained, the AI adapts in real time as engineers redirect, and the same reasoning session deepens across multiple exchanges. For incomplete or partially correct findings in complex environments, that distinction matters.

**Code-aware investigation is not front-and-center.** Traversal uses code and deployment data as inputs to their world model. What Resolve differentiates on is making that connection a first-class output: the code path, the commit, the PR, surfaced so the developer who owns it can act directly. Code-aware remediation is not a prominent part of Traversal's public narrative.

**No operational reporting.** Traversal has no equivalent to automated post-mortems, SLO reports, or on-call handover summaries. These are in active development at Resolve and delivering within months.

**No proactive optimization.** Traversal is reactive, triggered by alerts and incidents. Resolve is building continuous production signal analysis to surface reliability issues before they escalate.

**Granular governance not prominently documented.** Traversal's docs note read-only access, privacy safeguards, and access controls — which is a sound security posture. What their public documentation does not detail is granular RBAC, audit trails by investigation, and multi-tenant isolation at the level regulated financial services environments require. Resolve is SOC 2, HIPAA, and PCI-DSS compliant with team-scoped access controls built in and documented explicitly.

---

*Internal use only. Do not share externally.*
*Owner: GTM / Product Marketing*
*Next review: Q2 2026*

---

**Change log v2.0 (April 2026):**
- Softened "no follow-up / start over" claim across all sections; Traversal's docs confirm follow-up in Slack. Differentiation now focuses on statefulness and depth of the conversational debugging loop.
- Softened "incidents-only" framing; reframed as "strongest publicly around incident investigation and RCA."
- Softened "code is not central"; reframed as "code-aware remediation is not front-and-center in their public narrative."
- Reframed governance section: Traversal DOES document read-only access, privacy safeguards, and access controls. Changed to a documentation visibility gap (granular RBAC, audit trails not prominently featured), not a product absence claim.
- Kept and strengthened the read-only / agentless / security-first section — well supported by their docs.
- Removed "sync lag" as a stated fact; replaced with a discovery question.
- Reframed "single reasoning path risk" as competitive inference, not a documented limitation.
- Added acknowledgment that Traversal's Slack integration is more central than prior draft implied.
- Updated integration language to reflect Traversal's broad documented integration set.
