# Account POC Narratives — Detailed Templates
**Generated:** April 11, 2026  
**Source:** Attention call recordings + direct transcript analysis  
**Coverage:** 15 strategic accounts  
**Template:** Situation → Problem → Champions → Approach → Results/Current State + First Call Link

> **Evidence key:** Direct quotes from transcripts are in blockquotes. Inferred or synthesized data is marked [INFERRED]. Claims without call support are marked [NEEDS EVIDENCE].

---

## 1. Coinbase

**Status:** Active customer (production) | 146+ calls in Attention  
**First Call:** [Himadri Ghosh and Josh Grose — Feb 3, 2025](https://app.attention.tech/conversations/12e63ac0-5bf7-4af7-86a5-4055a257abc0)

### The Situation
Coinbase operates one of the highest-stakes production environments in the crypto industry — any downtime or latency incident translates directly to user fund risk and regulatory exposure. They run a massive distributed infrastructure of Kubernetes (EKS) clusters with thousands of microservices across hundreds of engineering teams. On-call rotations mean engineers may be responsible for services they haven't touched in 6 weeks, making context and knowledge transfer critical. Incident documentation is a regulatory requirement, not just a best practice. Their Platform Engineering org is responsible for reliability across the whole company, with a central SRE/incident management function complemented by embedded SREs in each product area.

### The Problem
The core pain is the complexity of troubleshooting in a highly distributed microservices environment where service ownership is fragmented across hundreds of teams.

> *"The biggest pain point is the troubleshooting part, which basically we have multiple microservices which communicate, and this is a large system so it might be some issue with some downstream services which is impacting the services. So yeah, that takes a lot of time to go through all the logs and then understand where the problem is happening and then again filter the another dependent service logs and that goes on until we basically find issue or that root cause."* — Himadri Ghosh, first call

> *"The main thing is the dependency on the other services which has different ownership within Coinbase and that takes longer to get information from the other team or connect to the other team."* — Himadri Ghosh

**What manual looks like:** When an alert fires, the on-call engineer acknowledges via Slack or PagerDuty, manually checks dashboards and logs for the affected service in Datadog, then begins tracing downstream dependencies — often requiring escalation to other team owners who may be in different time zones. 6,000+ alerts were generated in a 90-day production window, overwhelming on-call engineers. Even with automation in place, mean time to mitigation (MTTm) had not yet dropped measurably at the org level.

> *"Come into July, they're going to want to see that. This year, we have seen improvements in what we're receiving as value because right now we're investing a ton of effort. But we're not seeing mean time to mitigation drop across. Right, or yet?"* — Angelo Marletta

Additional pain: CloudWatch and CloudZero MCP connections blocked pending security review, and Confluence runbooks are often stale — creating trust erosion ("If I can't trust what it's showing me, I go back to doing it myself").

### The Champions

**Angelo Marletta** — Sr. Director, Platform Engineering  
Champion of the Resolve deployment. Cares about democratizing incident knowledge and getting all engineers — not just the most experienced — to resolve incidents quickly. Driving the expansion to proactive channel participation (surfacing signals *before* a page fires). Set a July deadline to demonstrate MTTm ROI.
> *"My goal is 50% aspirationally for all [incident types]."* (on MTTR reduction)
> *"My goal is that every single incident, regardless of severity, incident bot will kick off Resolve… and it gets to, as per the percentage, a faster root cause."*

**Chris Mueller** — Engineering Manager, Platform  
Acts as bridge between technical and business stakeholders. Focused on procurement, ensuring legal/contractual processes don't block reliability work. Pushing hard to close the expansion.
> *"I'm pushing as hard as I can. This is a movable force. I'm making some headway."*

**Raymond Sohn** — Engineering Lead  
Focused on usage metrics, adoption tracking, and ensuring Resolve surfaces the right signals. Participates in weekly cadence calls on metrics and UI/UX feedback.

**Troy Dai** — Infrastructure / Platform Engineering  
Technical champion focused on AI-assisted incident diagnosis in Kubernetes and networking environments. Specifically interested in helping junior engineers with context they don't have.
> *"[AI should help] junior engineers who may not have the experience to distinguish between trustworthy and suspicious information during debugging."*
> *"[AI could] bridge the gap in operational skills between infrastructure engineers and service owners by providing quick access to relevant data points."*

**Mike Beasley** — Infrastructure Lead  
Senior infrastructure leader engaged in broader org-wide rollout strategy. [NEEDS EVIDENCE — limited transcript data for direct quotes]

**Bassim Sadik** — Engineering Lead  
Introduced as a new champion for expanded deployment to Routing and Compute teams. [NEEDS EVIDENCE — limited transcript data]

**Bryan Gough** — VP Engineering [NEEDS EVIDENCE — named in org context but limited direct call data available]

### The Approach
Coinbase began with a discovery call in February 2025, followed by a structured pilot. Resolve was deployed in shadow mode — running investigations in parallel with existing manual processes — before going live in Slack incident channels. 

**Integration stack:** Datadog (logs, metrics), Kubernetes (topology, deployments, EKS), Slack (Resolve bot in incident channels), PagerDuty (alert source). GitHub/Confluence integrations added for runbook and code context.

The deployment expanded from the Core Reliability and embedded SRE teams (Chris Mueller, Angelo Marletta's org) to include Routing and Compute teams (Brett Inman's org) and the ROC (Reliability Operations Center). Office hours were established as a recurring touchpoint for engineers to learn and give feedback directly.

**Key milestones:**  
- Feb 2025: First call with Himadri Ghosh's team  
- Oct–Nov 2025: Weekly cadence established; onboarding Routing & Compute; usage metrics reviews  
- Nov 2025: Office hours launched (20+ attendees); Bassim Sadik intro call for expanded teams  
- Mar–Apr 2026: Leadership syncs at VP level; enterprise-wide deployment scoping discussions

### The Results
Coinbase is Resolve's most mature production deployment. Per data shared in leadership syncs and the Coinbase POC documentation:

- **~60% faster root cause analysis** for Resolve-assisted incidents vs. manual
- **Average investigation time: 15 minutes** vs. 35 minutes without Resolve
- **83 weekly active engineers** using Resolve in incident response (as of late 2025)
- **206 total users** onboarded
- **41 back-testers** running automated incident pattern validation (up from 19)
- Positive feedback trend: "I'm seeing new names every day, logging in and invoking Resolve… we are seeing positive feedback as folks are actually thumbs upping more than before." — Angelo Marletta

**Pending milestone:** Angelo's July 2026 commitment to show org-wide MTTm improvement. CloudWatch/CloudZero MCP approvals are the key unlock for expanding coverage.

---

## 2. Millennium Partners (MLP)

**Status:** Active customer (closed) | 63+ calls in Attention  
**First Call:** [MLP - Resolve AI: POC Alignment with Han Oh — Aug 29, 2025](https://app.attention.tech/conversations/54ab2f67-0f91-4b4f-a4fe-f9ebaa7d27ac)

### The Situation
Millennium Partners LP (MLP) is a leading global multi-strategy hedge fund with over $50B AUM. Their operations span multiple data centers across the US, EMEA, and APAC with approximately 350–400 technology and infrastructure engineers globally. Their ECC (Enterprise Command Center) processes 1,500 alerts per week out of a total 70,000 weekly alerts across the firm. This volume generates 20–30 major incidents ("bridges") per week — approximately 80 per month. Like all financial firms, MLP operates under strict data residency and regulatory requirements. Trading system reliability is existential: any downtime during market hours has direct financial and reputational consequences.

### The Problem
MLP's incident response is characterized by mass escalation, fragmented data, and siloed ownership — a structural problem that cannot be solved by hiring more engineers.

> *"Everything is getting 20 to 30 pings per day."* — MLP engineer

> *"We need to double every X year. We cannot keep on doing that."* — Rob Cherry (on headcount scaling)

> *"You get on these calls and you're just sitting there waiting for someone to be paged out to join the bridge on a team. You don't have access into their system."*

> *"You have 40 people on a call, only 6 speak. For about an hour and 15 minutes, people are like, yeah, has anyone checked the firewall?"*

**The "silent VIP" problem** — perhaps the most striking example of where the current process fails:
> *"The most painful issue we have isn't a big outage... the problem comes in, engineer starts working, it doesn't tell anyone... and then we find out seven days in that a VIP has had a problem for seven days. No one knew anything about it."*

**What manual looks like:** When a bridge is called, 40+ engineers join; only a handful are relevant. The incident commander works through teams sequentially — "has anyone checked X?" — while most participants wait. Data is fragmented across ServiceNow, Grafana, OpenSearch, and team-specific tools. No single engineer has full cross-domain visibility. Tech support handles ~500 tickets per day with the same manual escalation pattern.

> *"The challenge is hierarchical organizational structure, meaning that things are bouncing or having to go from team to team to team."*

**The ROI framing MLP uses themselves:**
> *"The majority of the benefit that they're gonna get is from headcount avoidance and reducing outage minutes."*
> *"Result pays for itself if we cut 50% of ECC outage minutes, which Rob believes is conservative."*

### The Champions

**Rob Cherry** — Head of Infrastructure / Operations (Rob C)  
Primary executive champion. Outcome-focused, not interested in product details — cares about ROI in numbers.
> *"He only wants to see pages with numbers that have to do with how much he has to pay or how much he's gonna make."*  
Drove aggressive adoption: "If you don't have it in Resolve, then it's on you. You made a mistake by not giving [that information to the system]."

**Pat Lenihan** — Engineering Lead, ECC  
Technical operator, most hands-on with the Resolve deployment. Focused on practical integrations and daily use.

**Daniel Ngo** — Tech Support / ECC  
Lead for the ECC use case. Cares about ticket volume reduction and eliminating the "silent incident" problem.

**Joshua Harris** — Infrastructure Lead  
Focused on the Resolve + ECC data integration and AWS infrastructure connectivity.

**Ricardo Sanchez** — Senior Engineer  
Deep technical integrations owner. Focused on auth, on-prem deployment, and the MCP layer.

**Luca Mihailescu** — Engineering Lead  
Works alongside Ricardo on technical implementation. Auth, OIDC, and Proxy setups.

**Anindya Chakraberti** — CISO  
The security gatekeeper. Data residency is non-negotiable — no operational data leaves the environment. Full audit trails required. Specifically worried about portfolio manager data isolation:
> *"We have to be extremely careful when we are building these things... if you have memory of an interaction with one portfolio manager and you leak that to another, it's game over."*

**Rob N** — Senior Executive (CTO/CIO level)  
Executive sponsor. Attended final POC readout. Wants the strategic partnership story and roadmap alignment.

**Han Oh** — Engineering (original first POC contact, Aug 2025)

### The Approach
MLP deployed Resolve via **Satellite** — on-premise data plane deployment required by data residency and security policy. This was a significant technical undertaking: Resolve's team built and standardized the Satellite deployment model specifically for MLP, solving for Microsoft Entra and Ping OIDC authentication, proxy settings, and on-prem MCP server scaffolding.

**Primary use case: ECC (Enterprise Command Center)** — automating triage of the 1,500 weekly alerts routed to the ECC, reducing the number of unnecessary bridge escalations.

**Integration stack:** ServiceNow (ticketing + CMDB), Grafana (monitoring), OpenSearch (log correlation), Slack (notifications), AWS (data plane connectivity).

**Key milestones:**  
- Aug 2025: POC scoping calls with Rob Newton and Rob Cherry  
- Sep 2025: POC alignment, success criteria defined; in-person sessions begin  
- Oct 2025: CISO conversation (Anindya Chakraberti); ServiceNow integration deep dives; legal finalization  
- Oct 2025: POC readout dry run; pricing and legal finalization  
- Nov 2025: ECC integration sessions; All Hands AI demo (60+ engineers)  
- Mar 2026: Multiple in-person on-site sessions at MLP; expansion planning  
- Mar 2026: Internal discussions about enterprise-wide scoping (alongside Salesforce and Coinbase)

The in-person engagement was extensive:
> *"Wide engagement. A lot of people have seen it. Literally we know more than a hundred people have seen Resolve."*
> *"All of his directs have been involved in conversations this week with us."*

### The Results
MLP is a closed customer with strong engagement across the executive and engineering layers.

- **50% reduction in ECC outage minutes** in the 700 scoped ECC cases during POC
- **Achieved effective automated investigations in live incidents within 2–3 weeks** of deployment (faster than anticipated)
- **Headcount avoidance** quantified at 2–3 FTEs across the org
- **Break-even at 3% productivity gain; target is 10–20%**
- **100+ engineers** exposed to Resolve; 70% of infrastructure executives engaged
- Rapid iteration loop: *"You tell us at 9pm, we fix at 1am"* — Resolve team responsiveness cited as key differentiator

**Roadmap priorities for expansion:** Multi-domain investigation automation, intelligent escalation management, cross-system correlation across network/server/application, and knowledge democratization to enable junior staff to perform expert-level troubleshooting.

---

## 3. Zscaler

**Status:** Active deployment — POC / expansion (Project Lighthouse) | 120+ calls in Attention  
**First Call:** [Zscaler / Resolve - Updates on Pilot — Jan 30, 2025](https://app.attention.tech/conversations/a461466f-4239-4e58-a968-9db7c98c8638)

### The Situation
Zscaler is a global cloud security company providing zero-trust network security to enterprise customers worldwide. Their internal infrastructure is a complex hybrid: bare-metal/VM environments for ZIA (Zscaler Internet Access, fully on-prem), AWS for other services, multiple global clouds with geographic regions (SV = Silicon Valley, TK = Tokyo, AM = Amsterdam) and environments (ZSPreview, ZSQA, production). They have four distinct operational teams that touch incidents: **CRE (Customer Reliability Engineering)** handles escalations and bugs; **TDO (Technical Duty Officers)** are incident commanders; **MIM (Major Incident Management)** runs major incidents; and **CSM** handles customer escalations. Each team has different relationships with alerting data and the incident timeline. Project Lighthouse is Zscaler's active, named internal initiative to reduce MTTD (mean time to detect) — with explicit executive sponsorship and budget.

### The Problem
The core contradiction: Zscaler sells zero-trust security automation to its customers, yet their own internal incident response is highly manual.

> *"Somebody actually manually SSHes into each specific node and manually downloads logs and then opens them up on their laptop."*

**Detection diagnosis is acknowledged as their #1 problem:**
> *"Detection diagnosis is our major problem still."*

Alert latency on Z4Z (their internal anomaly detection for data center health) runs 30–45 minutes — meaning by the time MIM is engaged, the incident has often been live for nearly an hour. Multi-team coordination is friction-heavy: CRE, MIM, TDO, and CSM each maintain their own incident view, with no shared structured timeline.

**What manual looks like:** Engineers SSH into specific nodes to fetch debug logs, open them locally, then correlate manually across Cloud Fuse dashboards, ZDX/Z4Z outputs, and Jira tickets. Knowledge is tribal — only a few architects know the true ZIA topology; documentation is often outdated.

> *"We want help in terms of faster debugging and troubleshooting for the live incident. We also wanted to kind of draw the pattern much accurately from the past existing data so that way it'll help us in terms of troubleshooting the new issues."*

> *"The value is once I have the debug, how much of data I could extract out of it saying that this is a problem. Analysis part is what [matters]."*

> *"I'd love to get the engineering team to start to feed more accuracy into something like Resolve so that we can interrogate right the way up to support."* — Duncan Winn

### The Champions

**Chris Umbel** — Senior Engineering Leader (Resolve knowledge graph owner)  
Primary technical champion. Owns the mapping of Zscaler's unique environment (custom jargon, ZS1 ≠ log label, etc.) into Resolve's knowledge graph. Cares about correctness and knowledge curation.
> *"ZS1 doesn't actually show up in logs, right? So this is where I do things like lay out synonyms that map to what we actually use when we speak and to what are the actual values that you would find in logs or in labels."*

**Manali Shrivastava** — Strategy & Operations Lead, Production Engineering  
Integration lead for the Resolve deployment. Drives adoption alignment across teams, manages Resolve AI ops sync cadences. Cares about cross-team coordination and security compliance for integrations.

**Duncan Winn** — Director, Production Engineering (reports to CTO)  
Senior engineering leader. Cares deeply about SRE best practices, knowledge sharing, and enabling newer engineers to investigate effectively. Champion for long-term Resolve integration.
> *"I'd love to get the engineering team to start to feed more accuracy into something like Resolve so that we can interrogate right the way up to support and support can ask questions like should I be concerned about this? What changed? What feature flags have turned on? Who saw this last?"*

**Shail Lande** — Engineering Leader  
Recurring weekly sync participant. Focused on incident response efficiency and tool integration.

**Prashant Anuj (Padmanabh Anuj)** — MIM (Major Incident Management) Lead  
Leads the MIM team that runs major incident (zinc) calls. Cares about MTTD reduction specifically — this is tied directly to his team's OKR under Project Lighthouse.

**Chris Hanaoka** — Engineering Leader  
Focused on post-incident reviews (PIR sessions) and deeper Resolve integration for the CRE team.

**Tyler Robbins** — Engineering Leader  
Independent stakeholder. Had 1:1 conversations with Resolve team about practical improvements to incident handling.

### The Approach
Zscaler's engagement has spanned over a year. The relationship started with paperwork, security reviews (architecture diagrams, pen test reports — minimum 1.5 month security evaluation), and Satellite deployment.

**First pilot:** Focus on integrating with Cloud Fuse (main observability/logging platform) and mapping Zscaler's unique bare-metal environment into Resolve's knowledge graph. Daily standups throughout the pilot (Jun–Jul 2025).

**Project Lighthouse (current):** Named initiative with executive sponsorship. Resolve is being evaluated as the core execution engine for Lighthouse. Key use cases:
- Z4Z alerts → automated investigation for tenant-specific incidents  
- Zinc channel support → Resolve bot invited into Slack zinc channels for live incident response  
- CRE team workflows → bug triage, escalation support, pattern recognition in backlog  
- TDO workflows → incident command, blast radius analysis  

**Jan 2026 workshop:** Large Zscaler team (~20 attendees) came on-site to Resolve's SF office for a full-day workshop to define use cases, map the knowledge graph, and align on the Z4Z POC scope.

**Integration stack:** Cloud Fuse (metrics, logs, dashboards), ZDX/Z4Z (internal alerting), Jira (bug tracking), Confluence (documentation), Slack (zinc channels), PagerDuty (alert routing), Grafana.

### Current State
Resolve is deployed and integrated with Cloud Fuse. CRE and TDO teams have access; initial training and workshops are underway. The Z4Z POC with tenant-specific alerts has kicked off. Some data sources (SME debug logs, code repositories) are pending final security review.

**Active blockers (as of March/April 2026):**
- Slack app approval still moving through security ticket process
- Knowledge graph needs ZIA architect validation for full accuracy
- Some log query gaps for specific services in dev environment
- Mapping clouds-to-observability sources needs refinement

> *"Risks: The main risks currently putting this deal at risk are organizational and process-related delays, particularly around security, access, and AI governance... these hurdles are making it difficult to move quickly."*

Executive communication is important: the board has AI as a strategic priority, and Resolve needs to be framed as an AI initiative.

---

## 4. Two Sigma

**Status:** Very early — exploratory | 2 calls in Attention  
**First Call:** [Two Sigma x Resolve AI: Overview & Demo — Mar 26, 2026](https://app.attention.tech/conversations/b7152d08-a77d-477e-acb0-eec594d2dd53)

### The Situation
Two Sigma is a quantitative hedge fund operating at the intersection of financial markets and technology, with offices in NJ and NYC. Like all quant funds, they operate under strict data governance and compliance constraints and have a strong internal engineering culture. The engagement is early — a single demo call was recorded in March 2026.

### The Problem
Limited signal due to Two Sigma's recording restrictions on previous engagement attempts. From the March 2026 call, the evaluation participants included engineers from multiple teams (Aleksandar Gyorev, Raj Jayakrishnan, Jason Chen, Mae Santos) suggesting a multi-stakeholder evaluation.

[NEEDS EVIDENCE — Two Sigma's side of earlier calls was not captured due to recording prohibition]

### The Champions
**Aleksandar Gyorev** — Engineering  
**Raj Jayakrishnan** — Engineering  
**Jason Chen** — Engineering  
**Mae Santos** — Engineering  

[NEEDS EVIDENCE — limited direct quotes from transcript available]

### The Approach
Resolve provided an overview and demo in March 2026 to a multi-person evaluation team. The call was structured as an initial technical introduction.

### Current State
Very early stage. No urgency signal captured. Given the quant fund profile, the likely path forward requires:
- Satellite/on-premise deployment architecture conversation
- Security and data residency documentation
- Addressing the internal build bias common at quant firms

---

## 5. BlackRock

**Status:** Early evaluation | 1 recorded call  
**First Call:** [Blackrock x Resolve — Sep 3, 2025](https://app.attention.tech/conversations/5b14d028-2d54-4589-a0c6-6cff15a156d7)

### The Situation
BlackRock is the world's largest asset manager with a technology organization operating at extraordinary scale. Their infrastructure is characterized by what their observability lead calls a "humongous rate of change" — driven not just by technical growth but by acquisitions, new product lines, and continuous regulatory changes, each of which drives infrastructure changes that can invalidate existing runbooks within weeks. They have ChatGPT Enterprise deployed internally and have been evaluating AI-powered tools across the organization.

### The Problem
**Rate of change makes manual RCA structurally impossible.** No static runbook can keep pace with BlackRock's infrastructure evolution. Human-driven root cause analysis can't keep up because the knowledge of "what changed" is distributed across hundreds of engineers and dozens of systems.

> *"Humongous rate of change."* — Baljeet, describing their infrastructure environment

Incident recovery times are "longer than we would usually expect" — not from a single crisis but as a persistent metric problem. At BlackRock's scale, even a 10% improvement in MTTR translates to meaningful risk reduction.

**The skepticism challenge:** BlackRock has been pitched by every AIOps vendor. Baljeet's instinct on seeing Resolve's demo was immediate, calibrated skepticism from a buyer who has been burned before:
> *"What you're saying to me immediately comes off as sounds too good to be true."*
> *"How is this different from all the other solutions in the market?"*

Jessica Guan also raised the build-vs-buy question directly, noting that ChatGPT Enterprise already has access to their internal data.

### The Champions
**Baljeet** — Observability Lead  
Technically sophisticated, skeptical but genuinely curious. Has deep experience with AIOps evaluation. Cares about proof over promise. Wants evidence of production-quality results, not demos.

**Raj Goel** — Engineering  
**Raghu Gella** — Engineering  
**Jessica Guan** — Engineering  

[NEEDS EVIDENCE — limited direct quotes for Raj, Raghu, and Jessica beyond Jessica's build-vs-buy question]

### The Approach
A single discovery/demo call in September 2025. The conversation covered Resolve's capabilities, integration approach, and how it differs from existing AIOps solutions. The call surfaced the "sounds too good to be true" credibility challenge as the primary obstacle.

### Current State
Early-stage. The engagement has not progressed beyond this initial call based on available data. Key prerequisites for advancement:
- Coinbase production case study as credibility evidence
- Clear differentiation from generic AIOps vendors
- Understanding of BlackRock's specific POC approval process

---

## 6. JPMC (JPMorgan Chase)

**Status:** Complex — two active opportunities | 25 calls in Attention  
**First Call:** [JPMC (Joe, Mike) — Apr 21, 2025](https://app.attention.tech/conversations/3d6ba6cd-52ce-4b75-b972-a9de30239cf0)

### The Situation
JPMorgan Chase is the largest, most systematically critical financial institution in the US — approximately 60,000 engineers supporting 4,000+ applications. Their SRE program is five years old, with pockets of high maturity alongside teams lagging due to scale and complexity. They currently use up to 20 different observability tools (Elastic, Splunk, Grafana/Tempo/Loki/Prometheus, Sumo Logic, Dynatrace, IBM Netcool, and others), with an active initiative to consolidate to 2–3 standardized platforms. They are actively exploring AIOps/GenAI for incident response and are building internal agent governance frameworks for the firm.

**Two separate opportunities are running in parallel:**
1. **Opportunity A (Isabella Disler's team):** Stalled — classified as "high risk" by the CSO office due to SaaS data exfiltration concerns
2. **Opportunity B (Eddie Wassef's team):** New contact as of March 2026, most promising path forward

### The Problem
**Engineering throughput crisis:**
> *"My engineering team has 50 priorities, maybe time for 20 of them."* — Eddie Wassef

**Data silos across 20 observability tools:** Engineers must jump between tools, manually gather evidence, and struggle to build a holistic incident view.
> *"I have not seen an AI solution that can pull from logs from one platform, metrics from another, traces from another, and then give you causal AI inferences off of all of that data living in separate places."* — Mike Kennedy

> *"The anomaly is because of the incredible amount of noise in the environment... just being a large complex organization and having an observability infrastructure that has to support that creates incredible amount of noise."*

**SaaS security classification blocks Opportunity A:**
> *"There is a security paper by [the] CSO warning against SaaS data exfiltration."*

**300+ question vendor questionnaire** — required before any formal evaluation can begin.

**Alert volume is overwhelming even with deduplication:** 50 million to 4 billion alerts/month, fed through IBM Netcool for correlation, still resulting in alert noise that overwhelms the triage team.
> *"When there's so many alerts, even if that alert fired, someone might not have looked at it."*

### The Champions

**Mike Kennedy** — SRE / Observability Lead  
Technical champion on Opportunity A. Cares about instrumentation adoption, reducing false positives, consolidating tools, enabling AI-driven RCA, and mapping critical user journeys to infrastructure.
> *"Adoption is just that they're instrumented and sending data to the platform. We can measure that at an individual deployed application component level."*
> *"The goal is not to have 20 different tools like we have now. The goal is to be maybe more, you know, two or three."*

**Alpa Stamp** — Central Strategic Services, Observability Platforms Lead  
Central platform owner supporting all JPMC business units. Cares about centralized observability and firm-wide reliability.
> *"We are the central platforms for observability, right? So we kind of need to... have a good positioning in the firm."*

**Sameer Shaikh** — Engineering  
Focused on knowledge graph architecture, multi-tenancy, and how Resolve learns from their environment.
> *"In the case of a multi-tenancy, right, how does it work? Like do you, would you have like a knowledge graph for the whole of JP or would it be at the application level?"*

**Isabella Disler** — Engineering Leader (Opportunity A)  
Originally a champion; now managing the "why not now" conversation as security classification blocked progress. Has been honest about the constraints:
> [Manages conversation about CSO "high risk" classification and timing challenges]

**Jeff Tyler** — AI Infrastructure / Agent Governance  
Building JPMC's internal MCP governance standards. A partnership conversation — Resolve needs to be involved as these standards are written, not respond to them after the fact.

**Eddie Wassef** — Engineering Leader (Opportunity B, March 2026)  
New champion, introduced March 2026. Exploring "BYO cloud" deployment models for agentic infrastructure. His 50-priority framing makes him the most commercially urgent champion.

**Marilyn Ramos** — Engineering (Opportunity B contact)

### The Approach
**Opportunity A timeline:**
- Apr 2025: First call with Joe and Mike — demo of alert investigation, integration questions raised
- Jun 2025: Large EOP team call (15+ JPMC attendees) — POC scope discussion
- Aug 2025: Security/technical demonstration, Q&A on architecture
- Sep 2025: POC discussion, business value call
- Oct–Nov 2025: Sameer Shaikh touchbase, network team discussion
- Dec 2025: Jeff Tyler relationship established (JPMC Jeff + team calls)
- Jan 2026: Isabella "why not now" conversation — CSO security classification surfaces
- Feb 2026: SRE team discussion with Jeff Tyler, Holly Bell, Arvind Ramalingam
- Mar 2026: Eddie Wassef intro — new opportunity opened

**Integrations discussed:** Splunk, Elastic, Netcool, Cortex (Grafana), Dynatrace, ServiceNow, Teams/Slack.

**POC structure proposed:** Satellite deployment starting with a few Kubernetes clusters; expand from initial scope based on results.

### Current State
Two parallel tracks with different statuses:

**Opportunity A (Isabella):** Security "high risk" classification is the primary blocker. Requires either escalation to CSO level or a new deployment architecture (satellite/BYO cloud). Jeff Tyler's agent governance framework may unlock or further complicate this.

**Opportunity B (Eddie Wassef):** Most promising. Eddie's "50 priorities, time for 20" framing makes him a strong champion for the engineering throughput narrative. BYO cloud framing suggests he's pre-solving the data residency concern. Needs to be progressed before momentum is lost.

---

## 7. Wells Fargo

**Status:** Early evaluation | 4 calls in Attention  
**First Call:** [Wells Fargo / Resolve AI - Josh & Nick demo — Nov 21, 2025](https://app.attention.tech/conversations/eba1f1df-bd9e-41d2-a99d-fb17d2bd5b43)

### The Situation
Wells Fargo is a major US bank in the middle of two simultaneous infrastructure transitions: (1) migrating to **OpenShift Container Platform (OCP/Red Hat)** and (2) consolidating data centers. Both transitions are happening concurrently, creating elevated incident risk during a period when the team's tooling and processes are also in flux. Current observability stack: Splunk (logging), AppDynamics (APM), ServiceNow (ITSM). Prasanth Nandanuru holds a Distinguished Engineer title — indicating this is being treated as a technical architecture decision, not just a tool purchase.

### The Problem
**Data sovereignty is the first and most significant concern:**
> *"This is like a production logs, right? That's all very proprietary, confidential information for the bank."* — Prasanth Nandanuru

Wells Fargo's production logs contain transaction data, customer behavior signals, and system state information that is highly regulated. Any tool that touches those logs triggers a compliance review.

**Migration complexity creating incident risk:** OCP migration and data center migration happening simultaneously create new failure modes and mismatched dependencies — incident rates typically spike during re-platforming.

**Splunk-centric architecture:** Deep Splunk investment means any new tool must integrate with Splunk at production quality or make a compelling case for routing around it (both technically and politically).

### The Champions
**Prasanth Nandanuru** — Distinguished Engineer, Consumer Technology  
Primary technical champion. Evaluating Resolve as an architectural decision, not just a tool evaluation.

**Josh Atencio** — Engineering (participated in first call)

[NEEDS EVIDENCE — limited direct quotes captured; 4 calls suggests slow-moving evaluation]

### The Approach
Discovery and demo calls through late November–early 2026. Focused on understanding Resolve's satellite deployment model, Splunk integration depth, and ServiceNow integration capabilities.

### Current State
Early evaluation. Key prerequisites:
- Satellite/on-premise architecture must be presented as the primary deployment model (addresses data sovereignty concern upfront)
- Splunk integration must be demonstrated at production quality
- ServiceNow integration is a hard requirement (ITSM of record)
- Need to identify who holds budget authority beyond Prasanth

---

## 8. Yelp

**Status:** Active POC — mid-April 2026 target | 9 calls in Attention  
**First Call:** [Resolve AI <> Yelp // Demo + Discussion — Oct 30, 2025](https://app.attention.tech/conversations/e2b9b55e-5254-449d-bc66-2170f73255a7)

### The Situation
Yelp is a consumer technology company in the middle of an observability modernization — migrating from **Zipkin** (legacy distributed tracing) to **ClickHouse + OpenTelemetry (OTel)**. They operate a custom service mesh and run GitHub on-premises. Their engineering team is structured with a reliability function that handles incident response across multiple service domains. Rob Johnson, the original champion who drove the initial evaluation, has left the company, and Giulio has taken over as primary champion. A competitive evaluation is actively underway.

### The Problem
**Observability tool migration creating a transition gap:** Engineers are operating in a hybrid state where some services report through old Zipkin tooling and others through new OTel. During incidents, engineers must check multiple systems depending on which service is involved — increasing MTTD and cognitive overhead.

**Organizational disruption from champion departure:** Rob Johnson's exit caused evaluation delays and required re-establishing momentum and context with a new owner.

**Active competitive evaluation:**
> *"We definitely have kind of an internal evaluation plan that we prefer to keep for ourselves."*  
At least one other vendor is being evaluated. Yelp is managing the process carefully to avoid vendor lobbying.

**Custom infrastructure creates integration complexity:** Non-standard service mesh and on-prem GitHub mean standard Resolve integrations may require additional configuration during POC.

### The Champions
**Giulio** — Engineering/SRE Lead (primary champion post-Rob Johnson departure)  
Driving the active POC with a self-imposed mid-April 2026 deadline. Set the timeline to coincide with the OTel migration.

**Rob Johnson** — Previous champion (departed)

**Yaro, Elntagka, Stradio** — Engineering participants (Oct 2025 demo call)

### The Approach
Introduced via demo in October 2025 (first call). Giulio took over and established a structured POC evaluation with a mid-April 2026 target. The POC is designed to run alongside the OTel migration so that the new incident response capability and new observability stack can be stood up together.

**Integration stack:** ClickHouse + OTel (new stack), custom service mesh, on-prem GitHub, Datadog [NEEDS EVIDENCE on full integration list].

### Current State
Active POC. Mid-April 2026 target is Giulio's self-imposed deadline. Key risks:
- Competitive evaluation in progress — at least one other vendor being compared
- On-prem GitHub and custom service mesh will surface integration edge cases
- Organizational stability depends on Giulio's continued ownership and focus

---

## 9. ADP

**Status:** Active evaluation — slow-moving | 5 calls in Attention  
**First Call:** [ADP x Resolve AI: Demo & Discussion — Mar 4, 2026](https://app.attention.tech/conversations/919e5b64-d1c4-4d2a-be62-6b8689e3fc9b)

### The Situation
ADP is one of the world's largest payroll and HR services companies, processing payroll for tens of millions of employees globally. Payroll processing incidents have near-zero tolerance — a major incident during a payroll window is existential for the company and its customers. ADP is simultaneously evaluating Resolve against **IBM AIOps** (parallel POC), migrating to **ServiceNow** (ITSM transition), and managing a large, bureaucratic enterprise procurement process. Sidcley Soares is an internal champion who must sell Resolve *upward* within ADP's structure — he does not have final purchasing authority.

### The Problem
**Massive incident war rooms:**
> *"Incidents regularly have 20 plus engineers."*

ADP's incident response is a company-wide event. Production incidents assemble large bridge calls of engineers from multiple teams — resource-intensive, disruptive, and slow.

**Knowledge fragmentation:**
> *"Production task requires stitching together knowledge from a variety of different tools... three or four different people who happen to know something."*

No single engineer has full context. Incident resolution requires finding the right people (who may be on PTO, in a different time zone, or deep in a project) and extracting knowledge that exists only in their heads.

**Institutional slowness:**
> *"ADP is 'lenta lenta' (slow, slow)."* — Sidcley Soares

Even a clear winner in a POC may take 6–12 months to reach contract at ADP.

### The Champions
**Sidcley Soares** — Internal Champion (running "internal sales")  
Driving the evaluation from inside ADP. Does not have final purchasing authority but is working to build internal alignment.

**Adi Raina** — Engineering (first call participant)  
**Patrick Chapman** — Engineering (first call participant)

[NEEDS EVIDENCE — limited direct quotes from Adi Raina and Patrick Chapman]

### The Approach
First call in March 2026 with demo and discussion. Running a parallel evaluation alongside IBM AIOps. ServiceNow integration is a key requirement given their ongoing ITSM migration.

### Current State
Sidcley is running internal "sales" to build support. IBM AIOps is the primary competitive threat (incumbent relationships, enterprise account team). ServiceNow migration is consuming attention of the same teams needed for evaluation. Sidcley needs executive air cover from Resolve's leadership to reach ADP's decision-makers.

---

## 10. Workday

**Status:** Active evaluation — strategic/complex | 5 calls in Attention  
**First Call:** [Resolve AI demo for Workday — Mar 3, 2026](https://app.attention.tech/conversations/6f4c5b0c-6cc1-4612-babc-c3f376b6768f)

### The Situation
Workday is an enterprise HR and financial software company serving 5,000+ enterprise customers. They have already built internal agentic AI — running on **Gemini** (Google) and **Bedrock** (AWS) — and have automated approximately **50% of their alert-based incident coverage** with internal tools. Their internal service architecture uses a proprietary configuration language called **"Espresso"** that describes their service topology. Gabe, an SVP, is the executive sponsor — indicating this is a strategic, FY27 budget-cycle decision about build vs. buy for incident response.

### The Problem
**The 50% problem — the hard half:**
> *"Everybody is exploring and experimenting what makes sense to build internally versus when do you go and partner with a vendor."* — Gabe (SVP)

Workday's internal agents handle straightforward, pattern-matching incidents. The remaining 50% requires cross-service reasoning, novel failure mode diagnosis, and deep understanding of Espresso-specific service topology — exactly the hardest problem in incident response.

**5,000-customer blast radius:** Every production incident can affect thousands of enterprise customers simultaneously, creating enormous pressure to resolve quickly.

**Proprietary Espresso language:** Any external tool that needs to understand Workday's service topology must reason about Espresso configurations — a non-trivial integration requirement.

### The Champions
**Gabe** — SVP, Executive Sponsor  
Decision-maker wrestling with the build-vs-buy question for FY27. Has authority to make this a strategic partnership, not just a tool evaluation.

**Chirag Andani** — Engineering (first call participant)  
**Vinay Pandella** — Engineering (subsequent call participant)

[NEEDS EVIDENCE — limited direct quotes beyond Gabe's positioning statement]

### The Approach
First demo call in March 2026 with Spiros Xanthos (Resolve CEO), Mayank Agarwal, and the product team. SVP-level engagement from the first interaction.

**Integration complexity:** Espresso integration needs to be on the engineering roadmap. Multi-cloud environment (GCP + AWS) adds investigation complexity.

### Current State
Strategic evaluation in progress. The FY27 budget cycle is the decision window. Resolve must win the positioning battle: not "replace what you've built" but "handle the 50% your internal agents can't touch." Espresso integration capability is the technical differentiator that unlocks this.

---

## 11. Ticketmaster

**Status:** Early evaluation — VP approval required for POC | 2 calls in Attention  
**First Call:** [Ticketmaster + Resolve AI intro — Oct 9, 2025](https://app.attention.tech/conversations/20528bd5-c687-4170-9054-eaabc8c94ad9)

### The Situation
Ticketmaster's central SRE team operates as an **internal consultancy** — embedded across product teams on 6–12 month engagements. They are stretched thin across many products and cannot function as a 24/7 incident response resource for every team. Their observability stack is fragmented across five tools: **Splunk Enterprise, Splunk Observability, Kibana, PagerDuty, and FireHydrant**. Ticketmaster's traffic profile is unique — massive, predictable spikes around major event sales (Taylor Swift, Super Bowl) plus unpredictable bot-driven spikes. Standard incident response tooling tuned for steady-state traffic doesn't match their architecture.

### The Problem
**Humans as knowledge bases:**
> *"I would prefer not using human beings as knowledge base."* — Yevhen (SRE Lead)

When an incident fires, the SRE team's first task is to find the engineer who *knows* this service, this failure mode, this codebase. The human is the runbook.

**Alert fatigue reaching terminal state:**
> *"At some moment, teams who got too many alerts, simply ignoring alerts."*

Engineers have learned to ignore alerting systems because the signal-to-noise ratio is too poor. Real incidents are being missed or delayed.

**Fragmented tool stack:** Five distinct tools require manual correlation across different query languages and latencies during incidents. Paging the wrong team and cascading escalations are a direct result.

**Event-driven traffic spikes:** A unique challenge — major events create predictable but enormous traffic spikes that stress the system in ways steady-state tooling doesn't address.

### The Champions
**Yevhen** — SRE Lead  
Technical champion. Clear articulation of the core Resolve value proposition. Driven to improve incident response but needs VP sign-off to proceed.

**Nicolo Taddei** — VP, SRE (must approve before POC can begin)  
Decision-maker. Attended the first call. Needs to be convinced before Yevhen can run the evaluation.

**Jessica Lair** — Engineering (first call participant, Ticketmaster UK)

### The Approach
First call in October 2025 with Nicolo and Yevhen. Positioned Resolve as the solution to alert noise, wrong-team paging, and the "rubber ducky companion" model for engineers investigating unfamiliar services.

### Current State
POC is gated on Nicolo's approval. The organizational mandate to improve incident response is real (C-suite awareness from high-profile incidents). The immediate path forward requires a follow-up with Nicolo to get formal POC approval.

---

## 12. Qualcomm

**Status:** Advanced — at pricing stage, 6-month security approval pending | 6 calls in Attention  
**First Call:** [Resolve.ai Introduction — Jan 7, 2026](https://app.attention.tech/conversations/3235d3b5-22cb-4627-8bc5-fafea0fd8980)

### The Situation
Qualcomm is the world's leading semiconductor company with complex engineering infrastructure. They have already built their own internal incident response AI called **"NOVA"** — essentially solving the same problem Resolve addresses. NOVA is deployed and in use. However, NOVA is hitting its ceiling, which is why they're evaluating Resolve. At the same time, Qualcomm evaluated **Datadog Bits AI** and found it disappointing. The firm is in a cost-reduction phase with active workforce reductions. Export controls create unique RBAC requirements — different teams have different access levels to different systems, and this is non-negotiable from a regulatory standpoint.

### The Problem
**Alert volume at semiconductor scale:**
> *"We have about half a million or so alerts per month resulting in about 70,000 incidents."*

500,000 alerts/month → 70,000 incidents. Manual triage at this volume is structurally impossible.

**NOVA has hit its ceiling:** The fact that Qualcomm is evaluating Resolve after building their own tool is the signal — the problem is harder than they expected, and internal tooling has limits.

**Datadog Bits AI disappointment:**
> *"Disappointing."* — Qualcomm's assessment of Datadog Bits AI after evaluation

**RBAC is non-negotiable:**
> *"RBAC is the biggest thing we need to address."*

Export controls require granular access control. Any tool deployed broadly without RBAC cannot meet regulatory requirements.

**6+ month security approval:** Even for established vendors like Datadog, Qualcomm's security review takes 6+ months.

### The Champions
**Anton** — SRE / Platform Lead  
Primary champion. Has done the internal selling and gotten to pricing. [NEEDS EVIDENCE — limited direct quotes from Anton in available transcripts]

[NEEDS EVIDENCE — other attendees from first call included engineers from both Qualcomm and Resolve teams]

### The Approach
Introduction call in January 2026, followed by progressive technical and commercial discussions. Reached pricing alignment with Anton's internal sponsorship. RBAC capability discussion is the critical technical thread.

### Current State
Commercial terms are in alignment. The deal is gated by: (1) 6-month security approval process and (2) RBAC capability readiness. Budget pressure from workforce reductions requires strong ROI documentation. Anton has done the internal selling — the path forward is through the security review.

---

## 13. Squarespace

**Status:** Early discovery — 1 call | 1 call in Attention  
**First Call:** [Resolve x Squarespace: Overview & Demo — Mar 23, 2026](https://app.attention.tech/conversations/0f5527ba-d997-4b17-ac82-4b8f25cbca54)

### The Situation
Squarespace is a website builder and commerce platform replacing **Lightstep** (legacy distributed tracing) with a modern observability stack. They operate across a **multi-cloud environment (GCP + AWS)**. Kevin Lynch, VP Engineering, has 12 years of tenure at Squarespace — deep institutional knowledge but also potential status quo bias. Other evaluation participants included Alban Dani, Roman Romanyak, and Scott McMillen.

### The Problem
**The "precursor signal" problem:**
A consumer lag alert that had historically been noisy (teams had learned to deprioritize it) turned out to be the precursor to a checkout failure. By the time engineers recognized the signal as real rather than noise, the customer impact had already occurred.

> *"Precursor signal"* — Kevin Lynch's framing for alerts that are individually ignorable but collectively catastrophic

**Documentation that doesn't exist where it's needed:**
> *"Documentation is never where it needs to be. There's always emails that are sent out that nobody reads."*

Institutional knowledge lives in email threads and Slack messages, not structured runbooks. Documentation culture is endemic to fast-moving engineering orgs.

**Lightstep migration creating a transition gap:** During migration, engineers operate in a hybrid environment where institutional knowledge about the old system may not apply to the new stack.

### The Champions
**Kevin Lynch** — VP Engineering (12-year Squarespace veteran)  
Primary champion. Articulated the "precursor signal" framing with precision — suggests deep familiarity with the problem. Has organizational authority.

**Alban Dani** — Engineering  
**Roman Romanyak** — Engineering  
**Scott McMillen** — Engineering

### The Approach
Single overview and demo call in March 2026. Early discovery — need more conversations to understand decision-making process, budget authority, and urgency.

### Current State
Very early. The Lightstep migration provides a natural urgency hook. Kevin's 12-year tenure means he could be either a strong champion (has authority and organizational understanding) or a risk (deep attachment to current tooling). Need to progress to a second discovery call.

---

## 14. Cribl

**Status:** Active evaluation — CEO and CTO engaged | 3 calls in Attention  
**First Call:** [Resolve AI — Thanks for Meeting at re:Invent — Dec 17, 2025](https://app.attention.tech/conversations/817d2afb-2aaa-49ae-b034-3fcabcef8280)

### The Situation
Cribl builds observability data pipeline software — they route, transform, and reduce observability data for enterprise customers. This means Ledion (CTO) evaluates tools at an exceptionally high technical standard. Cribl operates across **6,000+ single-tenant AWS accounts** (one per customer in many cases), creating a unique incident investigation challenge: each incident requires context within that customer's isolated AWS account. A **partnership angle** has been discussed — Cribl's data pipeline capabilities and Resolve's incident investigation capabilities could be complementary in a joint GTM story.

### The Problem
**The "toy" problem — from the harshest evaluator in the dataset:**
> *"I haven't seen one that actually is not a toy when it comes to real production value."* — Ledion (CTO)

This is genuine market skepticism from an industry insider who evaluates tools as part of his job. Most AI-powered incident tools demo impressively but fail in production.

**6,000 isolated AWS accounts:** Standard incident response tools assume a single environment. Cribl's architecture is 6,000 isolated environments — requiring multi-account investigation capability.

**Build-vs-buy actively on the table:**
> *"Why would we bother with an off the shelf solution... when we can fire up our own clankers and go build something in LangChain."*

Cribl has the engineering talent, AI familiarity, and domain expertise to build. Resolve must answer: what do you offer that Cribl can't build in-house faster?

### The Champions
**Ledion** — CTO  
Primary technical evaluator. The highest credibility bar in this dataset. If Ledion becomes a believer, the Cribl case study would be extraordinarily credible — an observability vendor who uses Resolve for their own ops.

**Chad** — Engineering (re:Invent meeting participant)  
**Sai Vadlamudi** — Engineering (first call participant)

[NEEDS EVIDENCE — limited direct champion quotes beyond Ledion's "toy" statement]

### The Approach
Met at AWS re:Invent (Dec 2025), followed by progressive conversations with CEO and CTO involvement. The partnership angle (Cribl sends data → Resolve investigates) is being explored alongside the pure customer evaluation.

### Current State
CEO and CTO are engaged, which signals strategic interest. The POC must be exceptional — Ledion's bar is "real production value," not a polished demo. The partnership framing may be more productive than a standard customer evaluation. Multi-account investigation capability must be demonstrated.

---

## 15. Veeva Systems

**Status:** Active evaluation — multi-contact, deepening | 3 calls in Attention  
**First Call:** [Resolve AI <> Veeva | Intro & Demo — Mar 9, 2026](https://app.attention.tech/conversations/e8a8f09d-4f29-4401-8133-2acdde67c67a)

### The Situation
Veeva Systems is a cloud software company serving the life sciences industry — pharmaceutical companies, biotech firms, and contract research organizations. HIPAA compliance is a hard requirement for any tool that processes their production data. Veeva operates a **non-Kubernetes, custom architecture** and uses **Mattermost** instead of Slack as their internal communication platform. They have a **Gemini mandate** (Google LLM as the standard for AI tools) and use **AWS, Check MK, Jira, and Confluence** in their stack. Dan Soble recently built a new centralized Production Operations function, suggesting organizational maturity investment in this problem. Their customer base runs clinical trials, regulatory submissions, and patient data management — meaning any downtime has real-world consequences beyond business metrics.

### The Problem
**2–3 hours RCA is the norm; 6 hours for database outages:**
> *"Very good engineers still takes them two to three hours."* — Murali Mohan

At 400–500 unique issues per month, even at 2 hours per incident (optimistic), this is 800–1,000 engineering hours per month consumed by incident response — the equivalent of 5–6 full-time engineers doing nothing but RCA.

**Complex escalation path:** Incidents escalate from ops → product team → developers, adding latency at each handoff. During deployments, alert storms occur when maintenance mode is missed — 150+ alerts that are effectively one incident requiring intelligent grouping.

**Non-standard architecture and tool constraints:**
> *"We do not use Slack inhouse. We use a very similar product called Mattermost."*

Gemini mandate requires AI tool compatibility with Google's ecosystem. HIPAA compliance creates additional security review overhead.

**Tribal knowledge dependency:**
> *"4–6 months before engineers feel comfortable on-call"* [INFERRED from follow-up email content]

### The Champions

**Murali Mohan** — SRE Lead  
Original champion. Quantified the pain precisely — 2–3 hours per incident for good engineers. Deeply familiar with the technical problem. Has been the relationship owner from the first call.

**Dan Soble** — Head of Centralized Production Ops  
Newer champion. Built the centralized prod ops function, which is the organizational home for this problem. His involvement signals executive investment in solving it.

**Mark Johnston, Virendra Dhapola, Vinayak Shenoi, Kent Guerriero, Jim Conning** — Engineering participants (first call)

### The Approach
First intro and demo call in March 2026 with the full engineering team (8 Veeva engineers + Resolve team). Positioned against Veeva's specific challenges: custom non-K8s topology, Mattermost integration, and HIPAA requirements.

**Key items resonated in first call:**
- Historical context and correlation with previous incidents
- Evidence-based citations building investigative trust
- Parallel with how experienced SREs naturally troubleshoot

**Open questions at end of first call:**
- Gemini requirement applicability to third-party solutions
- HIPAA certification and PII redaction capabilities
- Appropriate evaluation environment (starting with dev/test pipelines)

A follow-up with Dan Soble occurred March 25, 2026, focused on technical requirements and next steps for a POC.

### Current State
Early but deepening. Two calls in two weeks with expanding stakeholder involvement signals genuine interest. Blockers to resolve: Gemini compatibility (is a third-party AI tool allowed under the mandate?), HIPAA certification documentation, Mattermost integration feasibility.

---

## Cross-Account Summary

### Accounts by Stage

| Stage | Accounts |
|-------|----------|
| **Production / Closed** | Coinbase, MLP |
| **Active POC** | Zscaler (Project Lighthouse), Yelp (mid-April target) |
| **Advanced (pricing/security)** | Qualcomm |
| **Active Evaluation** | JPMC (2 opps), ADP, Workday, Veeva, Cribl |
| **Early Discovery** | Wells Fargo, Ticketmaster, Squarespace, BlackRock |
| **Very Early** | Two Sigma |

### Most Powerful Customer Quotes Across All Accounts

| Quote | Account | Speaker |
|-------|---------|---------|
| "I would prefer not using human beings as knowledge base." | Ticketmaster | Yevhen (SRE Lead) |
| "Somebody actually manually SSHes into each specific node and manually downloads logs and then opens them up on their laptop." | Zscaler | Engineer |
| "Very good engineers still takes them two to three hours." | Veeva | Murali Mohan |
| "My engineering team has 50 priorities, maybe time for 20 of them." | JPMC | Eddie Wassef |
| "Incidents regularly have 20 plus engineers." | ADP | Sidcley Soares |
| "We have about half a million or so alerts per month resulting in about 70,000 incidents." | Qualcomm | Anton |
| "I haven't seen one that actually is not a toy when it comes to real production value." | Cribl | Ledion (CTO) |
| "No operational data leaves our environment. Full audit trails are mandatory." | MLP | Anindya Chakraberti (CISO) |
| "You have 40 people on a call, only 6 speak." | MLP | MLP engineer |
| "Detection diagnosis is our major problem still." | Zscaler | Engineering lead |
