# Account Deep-Dive: Problem Narratives
**Generated:** April 11, 2026  
**Source:** Attention call recordings (Dec 2025 – Apr 2026)  
**Coverage:** 15 strategic accounts — Coinbase, Millennium, Zscaler, Two Sigma, BlackRock, JPMC, Wells Fargo, Yelp, ADP, Workday, Ticketmaster, Qualcomm, Squarespace, Cribl, Veeva  

---

## How to Read This Document

Each account section covers:
- **Company Context** — who they are and the Resolve relationship status
- **Key Contacts** — names and roles driving the evaluation
- **Engineering Initiatives** — what they're working on / building toward
- **Core Pain Points** — what's broken today, with verbatim quotes
- **Root Causes** — why the pain exists structurally
- **Why Now** — the urgency driver (internal deadline, leadership pressure, competitive event)
- **Obstacles to Resolve** — what's blocking or slowing the deal
- **PMM Signal** — what this account tells us about our positioning

---

## 1. Coinbase

**Status:** Active customer (production) | ~89 calls in Attention  
**Key Contacts:** Angelo Marletta (Sr. Director, Platform Engineering), Chris Mueller, Bryan Gough  
**Calls Analyzed:** 25+ including monthly leadership syncs and working sessions

### Engineering Initiatives
Coinbase runs one of the highest-stakes production environments in crypto — any downtime or latency incident translates directly to user fund risk and regulatory exposure. Their platform engineering team is scaling Resolve usage across multiple service domains, with a current push toward proactive incident channel participation (surfacing signals *before* a page fires) and deeper GitHub/Confluence integration.

### Core Pain Points
**Volume + Signal-to-Noise at Scale**
6,000+ alerts were generated in a 90-day window, overwhelming on-call engineers and making it nearly impossible to distinguish noise from critical signals. Even with Resolve in production, mean time to mitigation (MTTm) has not yet dropped measurably at the org level.

> *"Come into July, they're going to want to see that. This year, we have seen improvements in what we're receiving as value because right now we're investing a ton of effort. But we're not seeing mean time to mitigation drop across. Right, or yet?"*

**Security Approval Bottleneck on MCP**
CloudWatch and CloudZero MCP connections are blocked pending security review — a recurring theme where Coinbase's security posture (appropriate for a regulated financial institution) creates friction on expanding Resolve's data access. Engineers can see the value but cannot unlock connectors without security sign-off.

**Knowledge Retrieval at GitHub/Confluence Scale**
Resolve's code context retrieval works, but at Coinbase's repo size the relevance quality degrades. Engineers flag that runbooks in Confluence are often stale and that Resolve sometimes surfaces outdated resolution steps. This creates trust erosion: *"If I can't trust what it's showing me, I go back to doing it myself."*

### Root Causes
- Alert volume is a product of their micro-service architecture (hundreds of services, each emitting independently)
- No single engineer has full context across service boundaries — incident investigation requires assembling 3–4 people
- Security review processes are architected for traditional SaaS vendors, not agentic AI with live data plane access

### Why Now
Leadership has set a July milestone to demonstrate ROI on the Resolve investment. The pressure is explicit: the platform team is currently in a "we're investing heavily but not seeing MTTm results yet" phase and needs wins before the mid-year review. The proactive detection feature is positioned as the unlock — moving from reactive response to preventing pages.

### Obstacles
- MCP security approvals (CloudWatch, CloudZero) are stalled
- MTTm is measured org-wide, not per-incident-type — making attribution of Resolve's impact difficult
- Need to show Gough/Marletta a clear before/after metric story by July

### PMM Signal
Coinbase is the proof-of-production case — but the narrative must shift from "we deployed" to "we moved the metric." The July deadline creates an opportunity: **build a joint success story** that shows MTTm delta for Resolve-assisted incidents vs. non-assisted. This is the case study that sells every other financial services prospect.

---

## 2. Millennium Management

**Status:** Pre-sales / strategic prospect — no external calls recorded  
**Key Contacts:** Unknown (no external call recordings found)  
**Calls Analyzed:** 1 internal Resolve strategy meeting only

### Engineering Initiatives
Millennium appears as a named account in an internal Resolve discussion covering "Large Strategic Scale Requirements" alongside Salesforce and Coinbase. The internal framing describes Millennium as needing "enterprise-level discovery" and "more senior engineering coverage" before a formal evaluation can begin.

### Core Pain Points
No direct customer voice is available. Based on what is known about Millennium's infrastructure profile (large-scale quant hedge fund, extreme latency sensitivity, highly proprietary data environment), the anticipated pain points are:
- Ultra-low-latency incident detection and response in trading infrastructure
- Data sovereignty and air-gap requirements that would preclude standard SaaS deployment
- Internal tooling culture (hedge funds of this type often build everything)

### Root Causes
[NEEDS EVIDENCE — no external call data available]

### Why Now
Unknown from call data. Internal Resolve discussion suggests this is being treated as a strategic logo requiring a more deliberate, senior-led engagement.

### Obstacles
- No recorded external calls — engagement has not reached demo/discovery stage
- Likely significant data residency and security requirements given hedge fund context
- Internal build bias is common at firms of this type

### PMM Signal
Millennium is a whitespace account. Before building any messaging or collateral for this account, Resolve needs to run a proper discovery call. Flag for AE team: **prioritize getting a first call on record before any PMM materials are created.**

---

## 3. Zscaler

**Status:** Active deployment — POC/expansion phase | ~24 calls in Attention  
**Key Contacts:** CRE team, MIM team, TDO team, CSM team (multi-team evaluation)  
**Calls Analyzed:** 6 representative calls

### Engineering Initiatives
Zscaler is running **Project Lighthouse** — an internal initiative explicitly focused on reducing MTTD (mean time to detect). They have a structured team hierarchy: CRE (Customer Reliability Engineering), MIM (Major Incident Management), TDO (Technical Delivery Operations), and CSM. Each team has different relationships with alerting and incident data. Resolve is being evaluated as the core engine for Lighthouse.

### Core Pain Points
**Detection and Diagnosis Latency**
Alert latency of 30–45 minutes on the Z4Z product line is creating downstream customer impact. By the time the MIM team is engaged, the incident has already been live for nearly an hour.

> *"Detection diagnosis is our major problem still."*

**Manual Log Retrieval — Humans as Log Aggregators**
In the most striking verbatim from any call in this analysis, an engineer describes the current incident triage process:

> *"Somebody actually manually SSHes into each specific node and manually downloads logs and then opens them up on their laptop."*

This is a company that sells zero-trust network security — but their internal incident response is manual, node-by-node log collection. The irony is not lost on their engineers. This is a burning pain because it means MTTD is entirely dependent on which engineer is on call and how fast they can SSH into the right node.

**Multi-Team Coordination Friction**
With four distinct teams touching incidents, there is no shared, structured incident timeline. Each team maintains its own view of what happened and when. Post-incident reviews require reconciling four different logs.

### Root Causes
- Distributed, node-level architecture without centralized log aggregation at the right granularity
- Alert routing is configured for team boundaries, not incident causality
- Project Lighthouse has executive sponsorship but no tooling yet to support it

### Why Now
Project Lighthouse is an active, named initiative — meaning there is budget alignment and executive sponsorship already. The 30–45 minute detection gap is visible to leadership because it translates to customer SLA breaches on Z4Z. This is a "we have to fix this this year" problem, not a "nice to have."

### Obstacles
- Multi-team buy-in: CRE, MIM, TDO, and CSM all have to agree
- Deployment model questions (Zscaler is itself a security vendor — data residency expectations are high)
- Defining success metrics that span team boundaries

### PMM Signal
Zscaler is the **"irony account"** — a security company with manual log triage. The positioning that lands here: *"You wouldn't let your customers manage security manually. Why is your own incident response still manual?"* The Project Lighthouse framing is also useful: Resolve can position as the **execution engine for Lighthouse**, not a generic observability add-on.

---

## 4. Two Sigma

**Status:** Very early — exploratory | 1–2 calls  
**Key Contacts:** Distributed team (NJ + NYC offices)  
**Calls Analyzed:** 1 call

### Engineering Initiatives
Unknown — the discovery call was severely constrained by recording restrictions.

### Core Pain Points
Limited signal due to recording prohibition. What can be inferred from the call structure: Two Sigma operates distributed across NJ and NYC with significant compliance and data governance constraints typical of quantitative hedge funds.

> *"We are not allowed to be recorded."*

The call proceeded with Resolve's side recorded but Two Sigma's audio was not captured. This means no verbatim customer language is available.

### Root Causes
[NEEDS EVIDENCE]

### Why Now
Unknown — engagement appears inbound or early outbound with no urgency signal yet captured.

### Obstacles
- Recording restrictions eliminate the primary mechanism for Resolve (and Resolve AI the company) to capture and analyze call data
- Data sensitivity at a quant fund will likely require air-gapped or satellite-only deployment
- Internal build culture at Two Sigma is extremely strong

### PMM Signal
Two Sigma, like Millennium, requires a **compliance-first, build-vs-buy** conversation. The satellite architecture is the only credible path. Resolve needs a dedicated security/compliance one-pager for quant finance prospects before these conversations can advance.

---

## 5. BlackRock

**Status:** Early evaluation — 1 recorded call  
**Key Contacts:** Baljeet (Observability Lead), Raj Goel, Raghu Gella  
**Calls Analyzed:** 1 call (enterprise discovery)

### Engineering Initiatives
BlackRock is the world's largest asset manager with a tech org operating at extraordinary scale. Baljeet leads observability and is clearly technically sophisticated. The firm is mid-discussion on how to handle incident response at what he calls a "humongous rate of change" — both in their infrastructure and their business (acquisitions, new product lines, regulatory changes all drive infra changes constantly).

### Core Pain Points
**Scale and Rate of Change Make Manual RCA Impossible**
The core problem: BlackRock's infrastructure changes so frequently that any static runbook or playbook is obsolete within weeks. Human-driven RCA can't keep up because the knowledge of "what changed" is distributed across hundreds of engineers and dozens of systems.

> *"Humongous rate of change."* (Baljeet, describing their infrastructure environment)

**Recovery Time Exceeding Expectations**
Baljeet explicitly noted that incident recovery times are "longer than we would usually expect" — suggesting that while they have sophisticated monitoring, the time from detection to resolution is still a problem at their scale.

**Credibility Gap — "Sounds Too Good to Be True"**
BlackRock has been pitched by every observability and AIOps vendor. Baljeet's instinct when seeing Resolve's demo was immediate skepticism:

> *"What you're saying to me immediately comes off as sounds too good to be true."*

> *"How is this different from all the other solutions in the market?"*

This is not hostility — it is the appropriate reaction of a sophisticated buyer who has been burned by overpromising vendors. He has seen AI-powered incident tools that demo well and fail in production.

**POC Process Itself Is Difficult**
Even getting to a POC at BlackRock is a significant undertaking. The vendor evaluation process is rigorous, and the firm has been through enough failed evaluations that the bar for initiating one is high.

### Root Causes
- Infrastructure scale means no single human or team has full context
- Rate of change invalidates static documentation faster than teams can update it
- Prior AIOps solutions have created skepticism through overpromising and underdelivering

### Why Now
The urgency isn't from a single incident — it's structural. The "longer than expected recovery times" is a persistent metric problem, not a one-time crisis. At BlackRock's scale, even a 10% improvement in MTTR translates to meaningful risk reduction.

### Obstacles
- Deep credibility gap: Resolve must demonstrate *before* the POC, not just during
- POC approval process is significant (parallel to Qualcomm's 6-month security review dynamic)
- Raj Goel and Raghu Gella must be aligned with Baljeet before anything moves forward

### PMM Signal
BlackRock requires **evidence-first selling**. The Coinbase production case study is the unlock here: a regulated financial institution, at scale, with measurable results. The pitch cannot be "here's what Resolve does" — it must be "here's what Resolve did at Coinbase, here's the before/after, here's how we'd replicate it at BlackRock." The "sounds too good to be true" objection is the #1 blocker to address in collateral.

---

## 6. JPMC (JPMorgan Chase)

**Status:** Complex — two separate opportunities, one stalled on security | ~15 calls  
**Key Contacts:**  
- **Opportunity 1:** Isabella's team (stalled on security — "high risk" classification)  
- **Opportunity 2:** Eddie Wassef (new contact, introduced March 24, most promising)  
- Jeff Tyler's team (agent governance / MCP standards)  

**Calls Analyzed:** 8 representative calls across both opportunities

### Engineering Initiatives
JPMC is simultaneously running two relevant engineering workstreams:
1. **AI Infrastructure Governance** — Jeff Tyler's team is establishing agent governance frameworks and MCP standards across the firm. This is a new enterprise function being built in response to the explosion of AI tool adoption.
2. **Platform Modernization** — Eddie Wassef's team is exploring agentic infrastructure for engineering productivity, with a specific interest in "BYO cloud" deployment models.

### Core Pain Points
**Engineering Throughput Crisis**
Eddie Wassef put the engineering capacity problem starkly:

> *"My engineering team has 50 priorities, maybe time for 20 of them."*

This isn't a complaint about prioritization — it's a description of a structural deficit. JPMC runs one of the most complex financial infrastructure environments in the world, with hundreds of production systems, and their engineering teams are chronically oversubscribed. Incident response is one of the top consumers of unplanned engineering time.

**Security Blocked on SaaS Data Exfiltration**
The first JPMC opportunity (Isabella's team) is classified as "high risk" by JPMC's CSO office. The specific concern:

> *"There is a security paper by [the] CSO warning against SaaS data exfiltration."*

JPMC's security posture classifies any SaaS product that accesses production logs or metrics as a potential data exfiltration vector. This is not a Resolve-specific concern — it's a blanket policy that affects all AI-powered observability tools.

**300+ Question Vendor Checklist**
Even to begin a formal evaluation, JPMC requires completion of a vendor security questionnaire:

> *"There is a very long, vendor checklist that is a mandatory requirement for any engagement with JP Morgan Chase. It has over 300 questions."*

This is not a blocker unique to Resolve — but it means the cost of initiating a proper POC is extremely high on both sides.

**Agent Governance as an Emerging Blocker**
Jeff Tyler's team is building MCP governance standards that will define what agents can connect to what data sources at JPMC. Resolve's architecture — which requires connecting to production systems — must pass through this governance framework. The standards are still being written, which means the rules of engagement are not yet fixed.

### Root Causes
- JPMC's security architecture was built for a pre-AI threat model and is being retrofitted
- The engineering throughput problem is structural (too many systems, too few senior engineers)
- Multiple decision-makers across security, platform engineering, and AI governance create a multi-stakeholder sales problem

### Why Now
Eddie Wassef's introduction in March 2026 suggests renewed momentum — he's a new champion with fresh budget authority. The BYO cloud framing he brought up suggests he has already pre-solved the data residency objection in his mind. His engineering team's 50-priority backlog is a burning problem because unplanned incident work is the primary reason planned work slips.

### Obstacles
- Opportunity 1 (Isabella): Likely requires escalation to CSO level or new deployment architecture
- 300+ question vendor checklist must be completed before formal evaluation
- Jeff Tyler's MCP governance framework could accelerate OR block Resolve depending on how standards are written
- Eddie Wassef opportunity needs to be progressed before he loses momentum

### PMM Signal
JPMC has two different conversations happening. The **security conversation** (Isabella/CSO) requires a compliance deck and data residency documentation — this is table stakes. The **engineering productivity conversation** (Eddie) requires framing Resolve as an engineering throughput multiplier, not just an incident tool. The headline for Eddie's team: *"Give your engineers back 30% of their incident time."* The Jeff Tyler governance conversation is a **partnership opportunity** — Resolve should be in the room as MCP standards are written, not responding to them after the fact.

---

## 7. Wells Fargo

**Status:** Early evaluation | ~4 calls  
**Key Contacts:** Prasanth Nandanuru (Distinguished Engineer, Consumer Technology)  
**Calls Analyzed:** 4 calls

### Engineering Initiatives
Wells Fargo is mid-execution on two major infrastructure transitions:
1. **OCP Migration** — moving to OpenShift Container Platform (Red Hat OCP), a significant infrastructure re-platforming
2. **Data Center Migration** — consolidating or moving data centers, adding complexity to already-complex incident response

Current tooling: Splunk (logging), AppDynamics (APM), ServiceNow (ITSM). They are a Splunk shop with significant investment in that ecosystem.

### Core Pain Points
**Data Sovereignty / Log Confidentiality**
Prasanth was direct about the core concern:

> *"This is like a production logs, right? That's all very proprietary, confidential information for the bank."*

Wells Fargo's production logs contain transaction data, customer behavior signals, and system state information that is highly regulated. Any tool that touches those logs — even for analysis — triggers a compliance review.

**Migration Complexity Creating Incident Risk**
OCP migration and data center migration are happening simultaneously. During infrastructure transitions, incident rates typically spike (new configurations, new failure modes, mismatched dependencies). The engineering team is dealing with a higher-than-normal incident load precisely at the moment when their tooling and processes are also in flux.

**Splunk-centric Architecture**
Wells Fargo has deep Splunk investment. Any new tool must either integrate with Splunk or offer a compelling reason to route around it. This is both a technical integration question and a political one (Splunk has existing relationships at the executive level).

### Root Causes
- Regulatory environment means data governance requirements are non-negotiable
- Two simultaneous migrations create compounding complexity
- Legacy enterprise tooling (Splunk, AppDynamics, ServiceNow) creates integration dependencies

### Why Now
The OCP and data center migrations are creating a natural "burning platform" moment — the existing incident response process was built for their pre-migration architecture. As they re-platform, there's a window to upgrade the incident response process as well. The Distinguished Engineer title on Prasanth suggests this is being treated as a technical architecture decision, not just a tool purchase.

### Obstacles
- Data residency: Production log access requires compliance sign-off
- Splunk integration quality will determine technical viability
- ServiceNow integration is a requirement (it's their ITSM of record)
- Four calls suggests a slow-moving evaluation — need to identify who has budget authority

### PMM Signal
Wells Fargo needs a **financial services + Splunk integration** story. The satellite architecture is essential to discuss early — it's the answer to "our logs can't leave our environment." The migration context is the urgency hook: *"You're already re-platforming. This is the moment to also upgrade how you respond to incidents in the new architecture."*

---

## 8. Yelp

**Status:** Active POC — mid-April target | ~9 calls  
**Key Contacts:** Giulio (primary champion, leading pilot), Rob Johnson (left — organizational disruption)  
**Calls Analyzed:** 6 calls

### Engineering Initiatives
Yelp is in the middle of an observability modernization: migrating from Zipkin (legacy distributed tracing) to **ClickHouse + OpenTelemetry (OTel)**. This is a significant data pipeline change that affects how traces, metrics, and logs are correlated. Simultaneously, they operate a **custom service mesh** and run GitHub on-premises.

### Core Pain Points
**Observability Tool Migration Creating a Transition Gap**
The Zipkin → ClickHouse+OTel migration means Yelp's engineers are operating in a hybrid state where some services report through old tooling and some through new. During incidents, engineers must check multiple systems depending on which service is involved — this increases MTTD and creates cognitive overhead.

**Rob Johnson's Departure Created Organizational Uncertainty**
The previous champion left, causing a reorganization that delayed the evaluation timeline. Giulio has taken over, but the momentum and context that Rob had built needed to be re-established. This is a risk signal: if Giulio's priorities shift or he leaves, the deal may stall again.

**Internal Evaluation Secrecy**
Yelp is clearly running a competitive evaluation but is deliberately opaque about it:

> *"We definitely have kind of an internal evaluation plan that we prefer to keep for ourselves."*

This suggests Resolve is being compared against at least one other vendor, and Yelp is managing the process carefully to avoid vendor lobbying.

**Custom Service Mesh and On-Prem GitHub as Integration Complexity**
Yelp's non-standard infrastructure (custom service mesh, on-prem GitHub) means standard Resolve integrations may not work out of the box. The POC will surface integration edge cases that standard deployments don't encounter.

### Root Causes
- Observability tooling debt from a long Zipkin tenure
- Engineering leadership transition creating evaluation delays
- Custom infrastructure requiring bespoke integration work

### Why Now
Mid-April POC target is self-imposed — Giulio set this deadline. The OTel migration provides a natural forcing function: Yelp wants to stand up a new incident response capability *alongside* the new observability stack, not bolt it on later.

### Obstacles
- Competitive evaluation in progress (at least one other vendor)
- On-prem GitHub and custom service mesh will require integration work during POC
- Organizational stability depends on Giulio's continued ownership

### PMM Signal
Yelp's OTel migration is the timing hook. The pitch should be: *"You're rebuilding your observability layer. Build the incident response layer alongside it — don't end up with a new observability stack and the same manual response process."* Differentiation vs. competitor (likely Incident.io, PagerDuty, or FireHydrant) needs to be sharp given the active competitive eval.

---

## 9. ADP

**Status:** Active evaluation — slow-moving | ~5 calls  
**Key Contacts:** Sidcley Soares (internal champion, running "internal sales")  
**Calls Analyzed:** 5 calls

### Engineering Initiatives
ADP is running a parallel POC with **IBM AIOps** while evaluating Resolve. They are also mid-migration from a legacy ITSM to **ServiceNow**, which is creating process disruption and evaluation complexity. Sidcley Soares is not a buyer — he's an internal advocate who needs to sell Resolve upward within ADP's bureaucratic structure.

### Core Pain Points
**Massive Incident War Rooms**

> *"Incidents regularly have 20 plus engineers."*

ADP's incident response is a whole-company event. When something breaks in production at ADP (payroll processing for millions of employees is time-critical), the response involves assembling a large bridge call of engineers from multiple teams. This is resource-intensive, disruptive, and slow.

**Knowledge Fragmentation Across Tools and People**

> *"Production task requires stitching together knowledge from a variety of different tools... three or four different people who happen to know something."*

No single engineer has full context. Incident resolution requires finding the right people (who may be on PTO or in a different time zone) and extracting knowledge that exists only in their heads. This is a structural knowledge problem — not a tooling problem alone.

**IBM AIOps as a Parallel Competitor**
ADP is running a direct comparison between Resolve and IBM AIOps. IBM has existing relationships at ADP (enterprise account team, existing contracts). This is a difficult competitive dynamic because IBM's advantage is incumbency and enterprise sales infrastructure, not product quality.

**"Lenta Lenta" — Institutional Slowness**
Sidcley's characterization of ADP's decision-making:

> *"ADP is 'lenta lenta' (slow, slow)."*

This is both a cultural observation and a practical warning. ADP's procurement process, multi-stakeholder structure, and enterprise risk aversion mean that even a clear winner in a POC may take 6–12 months to reach contract.

### Root Causes
- Large, distributed engineering org with siloed knowledge
- ServiceNow migration consuming bandwidth of the ops teams who would evaluate Resolve
- IBM AIOps POC creates a "wait and see" dynamic

### Why Now
Payroll processing incidents have zero tolerance for extended downtime — ADP's customers are running payroll for millions of employees. A major incident during a payroll processing window is existential. This creates latent urgency that Sidcley can use to accelerate internally.

### Obstacles
- IBM AIOps competitive evaluation — IBM has incumbent advantage
- Sidcley needs air cover from a senior Resolve executive to reach ADP's decision-makers
- ServiceNow migration is consuming the attention of the same teams Resolve needs for evaluation
- Institutional slowness — budget and procurement cycles are long

### PMM Signal
The 20-engineer war room is the most visceral image in ADP's narrative. Every person on a major incident bridge is not doing planned work. The ROI calculation is simple: **if Resolve reduces a 20-engineer bridge to 5 engineers, that's 15 engineers × incident duration of unrecoverable engineering time saved per incident.** This is the headline for ADP. The IBM AIOps counter-narrative needs to be prepared: what does Resolve do that AIOps doesn't?

---

## 10. Workday

**Status:** Active evaluation — strategic/complex | ~5 calls  
**Key Contacts:** Gabe (SVP, executive sponsor)  
**Calls Analyzed:** 5 calls

### Engineering Initiatives
Workday has already built internal agentic AI — they are not a greenfield prospect. Their internal agents run on **Gemini** (Google) and **Bedrock** (AWS), and they have a proprietary configuration language called **"Espresso"** that describes their service architecture. They serve 5,000+ customers and have already automated approximately **50% of alert-based incident coverage** with their internal tools.

### Core Pain Points
**The Build-vs-Buy Decision Is Live and Unresolved**

> *"Everybody is exploring and experimenting what makes sense to build internally versus when do you go and partner with a vendor."*

Gabe (SVP) is personally wrestling with this. Workday has the engineering talent to build, the AI infrastructure already in place, and the institutional preference for internal tools. But they've also hit the ceiling of what their internal agents handle — the other 50% of incidents that their automation can't touch.

**The 50% Problem — The Hard Half**
Workday's internal agents handle the straightforward, pattern-matching incidents. What's left is the 50% that requires:
- Cross-service reasoning (incidents that span multiple service boundaries)
- Novel failure modes (never-seen-before patterns)
- Deep code context (requiring understanding of Espresso-specific architecture)

This is the hardest problem in incident response — and it's exactly where Resolve competes.

**Proprietary "Espresso" Language Creates Integration Complexity**
Workday's internal service architecture uses Espresso, a proprietary language. Any external tool that needs to understand their service topology must be able to parse and reason about Espresso configurations. This is a non-trivial integration requirement.

**5,000 Customer Blast Radius**
When Workday has a production incident, it can affect thousands of enterprise customers simultaneously. The pressure to resolve quickly is enormous — every minute of downtime multiplies across the customer base.

### Root Causes
- Strong internal engineering culture creates "we can build it" bias
- 50% automation plateau suggests they've picked the low-hanging fruit and are now facing the genuinely hard problems
- Multi-cloud architecture (GCP + AWS) adds complexity to incident investigation

### Why Now
Gabe's involvement at the SVP level suggests this is a strategic decision, not a tactical evaluation. Workday's AI roadmap is accelerating — they're building more agentic tooling across the board. The question they're answering now is: *should incident response be a build-or-buy decision for FY27?* Resolve needs to win this positioning battle before the FY27 budget cycle closes.

### Obstacles
- Internal build bias — Workday engineers believe they can build what Resolve does
- Espresso integration is a real technical blocker
- The existing 50% automation coverage means Resolve needs to demonstrate value on the *hard* 50%, not the easy cases

### PMM Signal
Workday is the **"build-vs-buy" archetype** account. The positioning is not "replace what you've built" — it's "**complement and accelerate what you've built**." Resolve handles the 50% your internal agents can't, without requiring you to rebuild your AI infrastructure. The Espresso integration needs to be on the engineering roadmap. If Resolve can demonstrate understanding of Espresso-based service topology, that is a material differentiator.

---

## 11. Ticketmaster

**Status:** Early evaluation — POC requires VP approval | ~2 calls  
**Key Contacts:** Yevhen (SRE Lead, champion), Nicolo (VP, must approve before POC)  
**Calls Analyzed:** 2 calls

### Engineering Initiatives
Ticketmaster's central SRE team operates as an **internal consultancy** — they are embedded across product teams on 6–12 month engagements, helping each team improve their reliability practices. This model means the SRE team is stretched thin across many products and can't afford to be a 24/7 incident response resource for every team.

Current tooling: **Splunk Enterprise, Splunk Observability, Kibana, PagerDuty, FireHydrant** — a fragmented, multi-vendor stack that requires manual correlation during incidents.

### Core Pain Points
**Humans as Knowledge Bases — The Core Indignity**

> *"I would prefer not using human beings as knowledge base."*

Yevhen's framing is the clearest articulation of the foundational problem Resolve solves. When an incident fires at Ticketmaster, the SRE team's first task is to find the engineer who knows this service, this failure mode, this codebase. The human *is* the runbook. This is unsustainable at Ticketmaster's scale (major live events, unpredictable traffic spikes).

**Alert Fatigue Leading to Alert Ignorance**

> *"At some moment, teams who got too many alerts, simply ignoring alerts."*

This is alert fatigue reaching its terminal state. Engineers have learned to ignore their alerting systems because the signal-to-noise ratio is too poor. This means real incidents are now being missed or delayed because the alerting systems have lost credibility.

**Fragmented Tool Stack**
Five distinct tools (Splunk Enterprise, Splunk Observability, Kibana, PagerDuty, FireHydrant) means no single pane of glass. During an incident, engineers must manually correlate data across systems — each with different query languages, different latencies, different contexts.

**Event-Driven Traffic Spikes Create Unique Incident Patterns**
Ticketmaster's traffic profile is unlike most SaaS companies — massive, predictable spikes around major event sales (Taylor Swift tour, major sporting events) and unpredictable spikes from bot activity. Standard incident response tooling is tuned for steady-state traffic, not spike-driven architectures.

### Root Causes
- Alert volume from a multi-tool stack with no unified alerting strategy
- SRE-as-consultancy model means no dedicated on-call team for each product
- Event-driven architecture creates incident patterns that pattern-matching tools miss

### Why Now
Ticketmaster's reputation damage from high-profile incidents (Swifties couldn't buy tickets) creates C-suite awareness of incident response as a brand risk. Yevhen has an organizational mandate to improve, but needs Nicolo's approval to run a POC. The urgency is real but the decision-making is gated.

### Obstacles
- Nicolo VP sign-off required before POC can begin
- Fragmented tool stack means Resolve needs multiple integrations (Splunk, Kibana, PagerDuty, FireHydrant)
- Event spike traffic patterns must be addressed in POC scope

### PMM Signal
The "humans as knowledge base" quote is the best articulation of Resolve's core value proposition in this entire dataset. It should be in the headline deck. For Ticketmaster specifically, the event-driven angle is important: **Resolve doesn't just help with steady-state incidents — it helps with the high-stakes, unpredictable events where you need answers in minutes, not hours.**

---

## 12. Qualcomm

**Status:** Advanced evaluation — at pricing stage, security approval pending | ~6 calls  
**Key Contacts:** Anton (SRE/Platform Lead, champion)  
**Calls Analyzed:** 6 calls

### Engineering Initiatives
Qualcomm built their own internal incident response AI called **"NOVA"** — essentially the same concept as Resolve. NOVA exists, has been deployed, and is being used. However, NOVA is being evaluated against Resolve for the use cases where NOVA falls short. Qualcomm is also implementing **RBAC (Role-Based Access Control)** as a top-priority capability requirement.

### Core Pain Points
**Alert Volume at Semiconductor Scale**

> *"We have about half a million or so alerts per month resulting in about 70,000 incidents."*

500,000 alerts/month → 70,000 incidents. This is a 7:1 alert-to-incident ratio, which means most alerts are either noise or grouped into incidents. The scale alone makes manual triage impossible — any human review process breaks down.

**NOVA Has Hit Its Ceiling**
Qualcomm built NOVA specifically to solve the incident response problem. The fact that they're evaluating Resolve means NOVA isn't solving it well enough. The specific gaps weren't fully articulated in the calls, but the decision to evaluate external tooling after building internal tooling is a significant signal: **the problem is harder than they expected.**

**Datadog Bits AI Disappointment**

> *"Disappointing."* (Qualcomm's assessment of Datadog Bits AI after evaluation)

Qualcomm evaluated Datadog's native AI capabilities and found them insufficient. This creates both an opportunity (Resolve can position against a known competitor) and a risk (Qualcomm may be suffering from AI fatigue — burned by multiple vendor promises).

**RBAC as Non-Negotiable**

> *"RBAC is the biggest thing we need to address."*

Qualcomm operates in a highly regulated industry (semiconductor IP, export controls). Different engineering teams have different access levels to different systems. Any incident response tool that doesn't enforce granular access controls cannot be deployed broadly.

**Security Approval Timeline**

> Security approval at Qualcomm takes 6+ months, even for established vendors like Datadog.

Qualcomm's security review process is lengthy. Being "at pricing" doesn't mean close to closed — it means the commercial terms are agreed but security approval could take 6 months.

**Budget Constraints and Workforce Reductions**
Qualcomm is in a cost-reduction phase with active workforce reductions. Budget for new tools is constrained, and any new purchase requires strong ROI justification.

### Root Causes
- Semiconductor hardware complexity creates extremely high alert volumes
- NOVA was built by engineers, not product teams — lacks the polish and reliability of a purpose-built product
- RBAC requirements stem from export control regulations (not just security preference)

### Why Now
The deal is at pricing — Anton has done the internal selling. The urgency is: close before the next budget freeze or headcount reduction creates a procurement pause. The 500K alerts/month problem isn't getting smaller as Qualcomm's chip portfolio grows.

### Obstacles
- 6-month security approval process — even with commercial terms agreed
- RBAC must be ready before broad deployment
- Budget pressure from workforce reduction context
- NOVA exists — Resolve needs to demonstrably outperform their internal tool

### PMM Signal
Qualcomm is the **"built it ourselves and it's not good enough"** archetype. The positioning: *"You've already validated the problem is worth solving — NOVA proves that. The question is whether you want to maintain an internal product forever or partner with a team whose entire mission is to solve this problem."* The RBAC capability gap is a tactical one that needs to be resolved (or roadmapped) to unstick the deal.

---

## 13. Squarespace

**Status:** Early discovery — 1 call  
**Key Contacts:** Kevin Lynch (VP Engineering, 12-year Squarespace veteran)  
**Calls Analyzed:** 1 call

### Engineering Initiatives
Squarespace is actively replacing **Lightstep** (legacy distributed tracing) with a modern observability stack, operating across a **multi-cloud (GCP + AWS)** environment. Kevin Lynch's 12-year tenure means he has deep institutional knowledge but also deep institutional attachment to how things have been done.

### Core Pain Points
**The "Precursor Signal" Problem — Noise That Becomes a Crisis**
Kevin described a specific incident that crystallizes the problem:

A consumer lag alert that had historically been noisy (teams learned to deprioritize it) turned out to be the precursor to a checkout failure. By the time engineers recognized the signal as real rather than noise, the customer impact had already occurred.

> *"Precursor signal"* — Kevin's framing for alerts that are individually ignorable but collectively catastrophic.

This is a sophisticated articulation of the alert fatigue problem: it's not that the alerting is wrong — it's that the *context* for interpreting an alert correctly requires cross-system reasoning that humans can't do in real time.

**Documentation That Doesn't Exist Where You Need It**

> *"Documentation is never where it needs to be. There's always emails that are sent out that nobody reads."*

Squarespace's institutional knowledge lives in email threads and Slack messages, not in structured runbooks. When Kevin says "emails that nobody reads," he's describing a documentation culture problem that is endemic to engineering organizations that move fast and don't prioritize knowledge capture.

**Lightstep → Modern Stack Migration**
The observability migration creates the same transition-gap problem as Yelp: during the migration, engineers are working in a hybrid environment where institutional knowledge about the old system may not apply to the new stack.

### Root Causes
- Alert fatigue from historically noisy monitoring has trained engineers to deprioritize certain alert types
- Documentation is unstructured and scattered (email, Slack, wikis without consistent structure)
- Multi-cloud architecture creates tooling fragmentation

### Why Now
Single early call — urgency is unclear. However, the Lightstep migration creates a natural window: *"You're already rebuilding your observability layer. This is the moment to build the institutional knowledge layer alongside it."*

### Obstacles
- Single call — need more discovery to understand decision-making process and budget
- Kevin's 12-year tenure could mean either strong champion (he has authority) or status quo bias (he knows what's worked)
- Lightstep migration consuming engineering bandwidth

### PMM Signal
The "precursor signal" framing Kevin used is extremely valuable for Resolve's positioning. It's a more sophisticated way to describe what Resolve detects — not just active incidents, but the pattern of signals that *precede* an incident. This language should be tested in broader messaging.

---

## 14. Cribl

**Status:** Active evaluation — CEO and CTO engaged | ~3 calls  
**Key Contacts:** Ledion (CTO, primary technical contact)  
**Calls Analyzed:** 3 calls

### Engineering Initiatives
Cribl is itself an **observability data vendor** — they build pipelines that route, transform, and reduce observability data. This means they understand the problem space deeply and are evaluating Resolve with extremely high technical scrutiny. They operate across **6,000+ single-tenant AWS accounts** — one account per customer in many cases.

There is a **partnership angle** that has been discussed: Cribl and Resolve have potentially complementary data pipeline + incident response capabilities.

### Core Pain Points
**Skepticism from Industry Insiders — The "Toy" Problem**
Ledion is not a typical buyer. He is a CTO of an observability company. His standard for "real production value" is exceptionally high:

> *"I haven't seen one that actually is not a toy when it comes to real production value."*

This is the harshest assessment in this entire dataset — from someone who evaluates tools daily as part of his business. It reflects genuine market skepticism about AI-powered incident tools: most demos look impressive, most production deployments disappoint.

**6,000 Single-Tenant AWS Accounts — Scale and Isolation**
Cribl's multi-tenant-by-design architecture (each customer gets their own AWS account) creates a unique operational challenge. An incident in customer environment #4,832 requires investigation within that account's isolated context. Standard incident response tools assume a single unified environment; Cribl's model is 6,000 isolated environments.

**Internal Build Bias — "Fire Up Our Own Clankers"**

> *"Why would we bother with an off the shelf solution... when we can fire up our own clankers and go build something in LangChain."*

This is the boldest build-vs-buy statement in the dataset. Cribl has the engineering talent, the AI toolchain familiarity, and the observability domain expertise to build their own incident response AI. The question Resolve must answer: what does Resolve offer that Cribl can't build faster themselves?

### Root Causes
- Cribl's unique 6,000-account architecture requires a purpose-built approach that generic tools don't address
- Their technical sophistication means generic demos don't land — they need to see production-quality AI reasoning
- Partnership framing may be the better approach than pure customer framing

### Why Now
CEO + CTO engagement suggests this is a strategic decision, not a tactical tool evaluation. The partnership angle (Cribl data pipeline + Resolve incident response) could be a compelling joint go-to-market story if the technical fit is confirmed.

### Obstacles
- Ledion's "toy" skepticism is the highest credibility bar in this analysis — the POC must be exceptional
- 6,000-account architecture requires Resolve to demonstrate multi-account investigation capability
- Build-vs-buy is actively on the table — Cribl's engineering team is actively considering building in LangChain

### PMM Signal
Cribl is simultaneously the **toughest technical audience** and a **potential strategic partner**. The pure customer sale is difficult. The partnership framing (Cribl sends data to Resolve, Resolve investigates incidents, together we offer pipeline + response) may be more productive. If Ledion becomes a believer, the Cribl case study would be extraordinarily credible — an observability vendor who uses Resolve for their own incident response.

---

## 15. Veeva Systems

**Status:** Active evaluation — multi-contact, deepening | ~3 calls  
**Key Contacts:** Murali Mohan (SRE Lead, original champion), Dan Soble (centralized prod ops, new contact)  
**Calls Analyzed:** 3 calls

### Engineering Initiatives
Veeva is a life sciences cloud company with strict **HIPAA compliance requirements** and a mandate to use **Gemini** as their LLM (Google partnership). They operate a **non-Kubernetes, custom architecture** and use **Mattermost** instead of Slack as their internal communication platform. Dan Soble leads a centralized production operations function that was recently formed, suggesting organizational maturation in their reliability practice.

### Core Pain Points
**2–3 Hour RCA Is the Norm (6 Hours for Database Outages)**

> *"Very good engineers still takes them two to three hours."*  — Murali Mohan

This is the most precise MTTR data point in this entire analysis. Even Veeva's best engineers spend 2–3 hours on root cause analysis for standard incidents. Database outages push to 6 hours. For a company serving life sciences companies — where clinical trials, regulatory submissions, and patient data management run on Veeva — a 6-hour database outage is a catastrophic customer experience.

**400–500 Unique Issues Per Month**
Volume that makes manual investigation unsustainable. Even at 2 hours per incident (optimistic), 500 incidents/month = 1,000 engineering hours/month consumed by incident response. That's 6+ full-time engineers doing nothing but RCA.

**Non-Standard Architecture — Gemini Mandate and Mattermost**
Veeva's Gemini mandate creates an integration dependency: Resolve's AI layer must be compatible with or complementary to Gemini. Their Mattermost environment means standard Slack-based incident notification workflows don't work out of the box.

> *"We do not use Slack inhouse. We use a very similar product called Mattermost."*

**HIPAA Compliance Layer**
Any tool processing Veeva's production data — which includes data from pharmaceutical and biotech companies — must meet HIPAA compliance standards. This is a security review requirement that goes beyond standard enterprise security questionnaires.

**Centralized Prod Ops as New Champion**
Dan Soble's emergence as a second key contact (alongside Murali) suggests organizational maturation — they're building a centralized function to own this problem. This is good for the deal (more organizational investment in solving the problem) and complex (more stakeholders to align).

### Root Causes
- Custom, non-K8s architecture means standard incident response tooling assumptions don't apply
- HIPAA creates compliance overhead that extends every vendor evaluation
- Gemini mandate locks them into Google's AI ecosystem for any tool they adopt
- 400–500 incidents/month at 2–3 hours each is structurally unsustainable

### Why Now
The formation of Dan Soble's centralized prod ops function is the urgency driver — leadership has invested in building the team, and now that team needs tooling. Murali's original pain (engineer-hours consumed by manual RCA) is now institutionally recognized. Budget is being allocated to solve this.

### Obstacles
- Gemini integration requirement — Resolve must work with or alongside Gemini, not compete with it
- Mattermost integration required (not Slack)
- HIPAA compliance review
- Custom architecture means standard deployment assumptions need to be validated

### PMM Signal
Veeva is the **highest-precision pain articulation** in the dataset. "Very good engineers still take 2–3 hours" is the exact framing for ROI conversations: *multiply (hours per incident) × (incidents per month) × (fully-loaded engineering cost) = the cost of your current incident response process.* The Gemini integration is not a blocker — it's a story: *"Resolve works alongside your LLM investment, not against it."*

---

## Cross-Account Synthesis

### The Universal Pain Pattern
Every account in this analysis is experiencing a version of the same structural problem:

> **Incident investigation requires assembling multiple humans to find and synthesize context that is distributed across systems, tools, and people — and this doesn't scale.**

The symptoms vary (alert fatigue, 2-hour RCA, 20-engineer war rooms, manual SSH log retrieval) but the root cause is identical: human knowledge is the bottleneck, and human availability is the constraint.

### The Six Buyer Archetypes
Based on this analysis, Resolve's accounts can be organized into six distinct buyer archetypes:

| Archetype | Accounts | Key Message |
|-----------|----------|-------------|
| **Production Proof** | Coinbase | "Here's what we achieved; here's the metric." |
| **Regulated Enterprise** | BlackRock, JPMC, Wells Fargo, Two Sigma, Millennium | "Data never leaves your environment; we've solved the compliance problem." |
| **Build-vs-Buy Evaluator** | Workday, Qualcomm, Cribl | "You've validated the problem. Stop maintaining the solution." |
| **Active Migration** | Yelp, Squarespace | "Upgrade your incident response while you upgrade your observability stack." |
| **Institutional Inertia** | ADP, Ticketmaster | "The cost of the status quo is quantifiable — let's calculate it." |
| **Deep Integration Required** | Veeva, Zscaler | "Custom architecture, custom deployment — we'll meet you where you are." |

### The Three Objections That Appear Everywhere
1. **"Sounds too good to be true"** (BlackRock, Cribl, Qualcomm) → Lead with customer evidence, not product claims
2. **"Our data can't leave our environment"** (JPMC, Wells Fargo, Veeva, Two Sigma) → Make satellite architecture the first thing discussed, not the last
3. **"We can build this ourselves"** (Workday, Cribl, Qualcomm/NOVA) → Reframe from product to platform: "Your engineers' time is better spent on your product than on maintaining incident tooling"

### Top Verbatims for Messaging
These quotes should inform Resolve's messaging across channels:

> *"Very good engineers still takes them two to three hours."* — Veeva (Murali Mohan) — **quantifies the cost of the status quo**

> *"I would prefer not using human beings as knowledge base."* — Ticketmaster (Yevhen) — **articulates the core value proposition**

> *"Incidents regularly have 20 plus engineers."* — ADP — **quantifies the resource cost of manual incident response**

> *"Somebody actually manually SSHes into each specific node and manually downloads logs and then opens them up on their laptop."* — Zscaler — **makes the manual process visceral and embarrassing**

> *"At some moment, teams who got too many alerts, simply ignoring alerts."* — Ticketmaster (Yevhen) — **describes alert fatigue reaching its terminal state**

> *"My engineering team has 50 priorities, maybe time for 20 of them."* — JPMC (Eddie Wassef) — **frames incident response as a throughput problem**

---

*This document synthesizes Attention call recordings from December 2025 through April 2026. All quotes are verbatim from recorded calls unless otherwise noted. Claims marked [NEEDS EVIDENCE] require additional customer validation before use in external materials.*
