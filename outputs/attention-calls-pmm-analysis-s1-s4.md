# Resolve AI — Attention Calls PMM Analysis
### S1–S4 Deal Stages | Feb–Apr 2026
_Synthesized from 25+ calls across LLoyds Banking Group, HSBC, TIAA, McKinsey, Adobe, DoorDash, Block/Square, ADT, Invisible, Upgrade, Bloom Credit, and others_

---

## How to Read This Report

Calls spanned four pipeline stages:
- **S1 (Discovery/Intro):** First or second calls — understanding the problem space
- **S2 (Demo/Deep Exploration):** Live demos, architecture deep-dives, evaluation framework set
- **S3 (POC/Pilot):** Active proof-of-concept or paid pilot running
- **S4 (Negotiation/Closed Won):** Commercial discussions, contracting, or closed deals

---

## 1. WHY WE WON (And Why Deals Are Progressing)

### The Core Win Pattern
Deals progress when Resolve can show — not just tell — what it actually looks like to trace a real incident from alert to root cause to PR. Every deal that accelerated to S3+ shared a common inflection point: a live demo moment where Resolve connected disparate signals (Terraform → Git → code commit → deadlock) autonomously. That demo moment converts skeptics.

### Specific Win Drivers

**"The ahh moment" — Autonomous investigation demo**
The single most consistent deal accelerator was showing a real incident investigation, not a toy example. When prospects saw Resolve trace a Postgres deadlock to a specific engineer's commit, identify a network-not-at-fault pattern that cleared 20 engineers from a bridge call, or find a Kubernetes pod restart cause across multi-repo context — deals moved.

> _"So it is kind of like that human replacing that human reviewer within like the observability process."_ — **Carla Hindley, Chief Data & Analytics Office, LBG (S1 → progressing)**

> _"Aja had been beating his head against a wall all day on an issue. He was debugging, couldn't solve it. And after sitting down with Resolve for a bit, he was able to come to root cause using the tool. So that's pretty cool."_ — **Internal Resolve sync, Adobe POC (S3)**

> _"Root cause found correctly. Nice."_ — **Adobe POC participant**

**Social proof from tier-1 logos**
Coinbase, DoorDash, Salesforce, Morgan Stanley, Zscaler, and Toast were name-dropped repeatedly and each time they silenced skepticism at financial institutions and large enterprises. TIAA explicitly said they would only move to POC after a reference call with a Morgan Stanley or Millennium Partners-scale deployment.

> _"If this is your bread and butter, that's what it is. Just implement it. Put your system integrations in. You should be able to show value in a week."_ — **Jay Rudrachar, Observability Lead, TIAA (S2)**

**The "no new system to learn" pitch**
Slack-native interface and the ability to do `/rca` directly from an alert thread — zero context-switching for on-call engineers — was a consistent progressor, especially with heads of SRE.

**Proof-of-value (POV) process as a sales differentiator**
The structured POV process (3-4 weeks, 3 use cases, ROI grounding before a single dollar is spent) reduced the activation energy for large enterprises. This framing also landed well at McKinsey:

> _"I like this entry package. That sounds good. And I think even the description says it's like each session includes like five turns, so I don't think it is as simple as just having a..."_ — **Krinal Manakiwala, McKinsey (S1)**

**"More leverage per engineer, not more engineers"**
The productivity framing resonated strongly with every engineering leader managing a scaling environment without headcount budget:

> _"Our system is probably gonna double over the course of the year if things go well, but our SRE team is not going to double in size and we're not gonna be able to afford to."_ — **Alexander Crettenand, Head of Software Engineering, ADT**

> _"Our teams are constantly being asked to do more with less."_ — **Krinal Manakiwala, McKinsey**

---

## 2. CUSTOMER PAIN POINTS (Verbatim Soundbites)

### Pain Theme 1: MTTR Crisis + Overcrowded Bridges

> _"Reliability is not achieved. We have more failures and we want to reduce them. MTTR is high — meantime to resolution takes us a long time. Customers act as canaries so they find the problem before we do. Our incidents have 20+ engineers on a single bridge."_ — **Anestis Samaras, Group Head of Data Science, LBG**

> _"MTTR is high, customers are your canaries. So they report issues before you find them. And you have massive bridges with 20+ engineers on them."_ — **HSBC CTO/Service Management (S2 demo)**

> _"Not getting a result in 30 minutes is like holy crap. Usually the whole thing will have been resolved in some short period of time, right? Like 15... something minutes maybe 20."_ — **Brandon Zimmerman, Senior SRE, Block/Square (S3 POC)**

### Pain Theme 2: Fragmented Tooling, No End-to-End Picture

> _"Our current environment is quite fragmented. We have different tools. There are some tools that don't have even basic observability at all. Some places we have Dynatrace, some places SignalFx, some places nothing."_ — **Jay Rudrachar, TIAA (S2)**

> _"What we don't have is a mature resolve capability where we know what's happening, what is broken, but we do not know why and how to go about it. That's where we spend the majority of time."_ — **TIAA Operations leader**

> _"The number biggest problem that we have is each team sort of understands what the challenges are, but we don't have the end-to-end picture."_ — **TIAA**

> _"The difficulty is... something gets output from Terraform, it relates to something that someone has configured in Git, it's across different repos identifying which repo, that pipeline is configured to someone where someone made the spelling mistake. Why this generated an error — I think that's a difficult problem to identify."_ — **Anestis Samaras, LBG**

> _"A lot of errors are kind of silent errors with no alerts."_ — **LBG**

### Pain Theme 3: Knowledge Silos & Onboarding Failure

> _"The key between these people and your production is fragmented knowledge that usually lies in meetings, in messaging, but also in runbooks that are not either present or always up to date."_ — **HSBC**

> _"With each new feature everything gets more complex and has more failure modes and it's rapidly becoming more than any individual person can easily keep a mental model of. And if you don't have a good mental model of the system, it makes it extremely hard to troubleshoot."_ — **Wayne Hill, SRE Manager, ADT**

> _"Nice. This is super helpful because we spend so much time building them [runbooks] and then they are not in the eye. So that's amazing. This one is going to be especially helpful."_ — **Saasha Mor, SRE, Adobe (S3 POC)**

### Pain Theme 4: Alert Fatigue & Information Overload (emerging)

> _"I'm getting a lot of comments around brevity missing... people are just starting to ignore Resolve in some cases, which is kind of tough to see because they're like, oh, like the on-call knowledge buddy answered my question and you know, it was like five lines..."_ — **Alex Danilychev, DoorDash SRE (S3 POC)**

> _"I myself have found it to be like a little information overload sometimes."_ — **Arin Champati, DoorDash**

### Pain Theme 5: Ownership Gaps & Patchwork Codebases

> _"My biggest frustration is lack of clear ownership on a lot of these areas."_ — **Kit Colbert, Engineering Leader, Invisible (S1)**

> _"It's pretty messy, to be totally honest. A lot of shifting ownership across different code areas. And because of that it's become a bit of a patchwork. It's not always clear who actually owns something."_ — **Kit Colbert**

> _"A lot of our GitHub repos don't require reviews or approval... like really basic stuff."_ — **Kit Colbert**

---

## 3. BUYER PERSONA ANALYSIS

### Primary Persona: The Enterprise SRE Leader / Platform Engineering Head
**Titles seen:** Head of SRE, Staff SRE Engineer, Engineering Manager (SRE), VP Platform Engineering, CTO of a business unit
**Company types:** Large financial institutions (LBG, HSBC, TIAA), top-tier tech enterprises (Adobe, DoorDash, Block/Square), mid-market tech (Invisible, ADT)
**Environment:** Multi-cloud, multi-tool, 200+ microservices, 15-50 person SRE team
**What they care about (in their words):**
- Reducing time-to-root-cause in P1/SEV1s
- Reducing the number of people on a bridge call
- Getting new engineers on-call faster
- Not adding yet another tool to the stack
- Security/compliance approvals (especially FSI)
- ROI with a clear multiple before committing budget

**Key quote from this persona:**
> _"You have a complete infrastructure, multiple types of deployments, multiple tools not just Splunk but others, multiple repos. And then you have a set of specialized skilled people now required to essentially first fathom and understand a very complex infrastructure, but also reason through it and solve alerts."_ — **Tom Ashford, Major Incident Management, HSBC**

---

### Secondary Persona: The Engineering Executive / Decision Maker
**Titles seen:** CTO (ADT), Group Head of Data Science (LBG), CTO of WPB (HSBC), Head of Software Engineering
**What they care about:**
- Scaling ops without scaling headcount
- Demonstrating AI ROI internally (they're also pitching this internally to CFO/Board)
- Risk of integration and data governance
- Competitive differentiation of their own org

**Key quote:**
> _"Our system is probably gonna double over the course of the year if things go well, but our SRE team is not going to double in size."_ — **Alexander Crettenand, ADT**

---

### Tertiary Persona: The On-Call Engineer / Power User
**Titles seen:** SRE, Staff Engineer, Oncall engineer
**Company:** Adobe (multiple teams), DoorDash, Block
**What they care about:**
- Speed — if it takes >20 min, it's already too slow
- Context-aware answers in the tool they're already using (Slack)
- Being able to steer the investigation when the AI is off-track
- Transparency into what the agent is looking at

**Key quote:**
> _"I wanna be able to be like, bang important, always look at runbooks every single time. Don't do this as early as possible, which I've tried to do as much as I can and it doesn't seem normal listening."_ — **Brandon Zimmerman, Block/Square**

---

## 4. DIFFERENTIATED CAPABILITIES THAT LANDED IN MESSAGING

### #1 — "We eliminate the unnecessary human reviewer"
This framing — specifically around removing the engineer who had to join a bridge call only to say "not my team" — resonated powerfully at financial institutions:

> _"It's replacing also the unnecessary human reviewer. Very common in banks — you have latency, you call up network, 70% of the time it's not network's fault, but you've still engaged one to two to three engineers from network that have to go and check and spend X time when it's actually completely useless. I'm able to preempt this because I can tell you non-network, it's this problem."_ — **Vasi Karkantzos, Resolve (with clear confirmation from LBG prospect)**

### #2 — "It operates in the tools you already have"
This framing differentiated Resolve from AIOps point solutions and from the "build your own" objection. The message "not a single source of truth, operates in your environment" landed every time:

> _"Resolve really helps because it doesn't have a single source of truth. It operates within the tools that you have and the environment that you have."_ — **TIAA call, prospect reaction: "I mean if you can solve UC1, that is fantastic. Show value in a week."**

> _"Resolve can go across all the different tools and kind of have that specialization and pull it all together."_

### #3 — "Production AI, not coding AI"
The distinction between Resolve and coding agents (GitHub Copilot, Cursor, Claude Code) was a recurring question that Resolve had to address. The "troubleshooting is non-deterministic" frame worked but needs to be sharper:

> _"Coding agents are more deterministic. Production troubleshooting is completely non-deterministic. You don't know which code path will be traversed, which service dependency is going to fail, which logs are going to be relevant."_ — **Vasi Karkantzos, HSBC demo**

### #4 — "Day-one value, not months of training"
The "useful from day one" message directly addressed the biggest objection — "it takes too long to calibrate":

> _"The idea is that results should be useful day one. It's not at its most effective form day one, but it is useful day one. Don't think of this as something that takes months for the agent to get up to speed."_ — **Spiros Xanthos, HSBC demo**

### #5 — "Knowledge graph + postmortem as living document"
The cited, hyperlinked postmortem report was a standout differentiator for power users at Block and Adobe:

> _"The thing that this tool does really well is it basically constructs an entire postmortem. And that's kind of what it does really, really well — it has a very cited postmortem where it's like, multiple of us have looked at it and we're like, geez, it has a lot of citations, it has a lot of links to all the stuff."_ — **Brandon Zimmerman, Block/Square (S3 POC)**

### #6 — "Engineer onboarding: on-call in 2 weeks not 6 months"
The onboarding story (UX designer at Resolve put on-call in 2 weeks) created a memorable, human-level illustration of value that engineering leaders responded to.

### #7 — Consumption-based pricing = "you only pay for work the agent does"
This framing reduced the barrier at every stage:

> _"You don't pay for software. You only pay for the work the agent does. You can decide how much to use it and where to use it."_ — **HSBC demo**

---

## 5. POSITIONING GAPS (Recurring Issues We Struggled to Answer)

### Gap #1: "How are you different from what we could build ourselves?" ⚠️ HIGH PRIORITY
This is the single most dangerous unanswered question across S1-S2 calls. Every large enterprise (HSBC, ADT, McKinsey) asked this directly, and Resolve's answers were high-level and not crisp.

> _"What do you do in that environment that we wouldn't be able to do ourselves? Or our own agents. Exactly. Got it."_ — **Petek Ergul, Service Management Lead, HSBC**

> _"Because like, what is gonna be the difference between me asking Cloud Code to connect to my GCP client and figure this out versus using your service?"_ — **Mayank Agarwal, ADT tech deep dive**

**The gap:** No "build vs. buy" proof point with real data. No counter-answer to "we have an AI team." Current answer is conceptual ("it's complex"). Needs to be: specific time/cost estimates to build comparable, plus the ongoing model training investment required.

---

### Gap #2: Proactive anomaly detection / "silent errors" ⚠️ HIGH PRIORITY
Multiple prospects — especially FSI — asked about proactive monitoring, not just reactive investigation. Current answer ("we don't do that, by choice") is honest but may lose deals where prospects have this as a requirement.

> _"Are you proactively looking at any logs and finding where there might be some abnormal behavior compared to what you would see historically?"_ — **Anestis Samaras, LBG**

**Resolve's response:** _"We wouldn't do that. I mean we can do that, but you have to ask me, and this is by choice. We don't wanna proactively ingest anything. We query your logs opportunistically once triggered."_

**The gap:** Proactive vs. reactive is a fundamental buyer segmentation question. Prospects comparing to Dynatrace/Datadog AIOps expect proactive anomaly detection. We need a clear message on where we play and why the reactive/triggered model is *better*, not just different.

---

### Gap #3: Change detection breadth — "70% of your changes aren't covered" ⚠️ HIGH PRIORITY (Enterprise)
TIAA flagged this repeatedly and it nearly stalled the deal:

> _"What I am seeing in your roadmap is all software change — GitHub, GitLab, Kubernetes, that's it. That is only 30% of our change. 70% you're not even covered here."_ — **Jay Rudrachar, TIAA**

> _"Change could be a security configuration change, network configuration change, device changes, hardware change, software change, configuration change, cloud IAM policy change. How do you collect all the changes across enterprise?"_ — **TIAA**

**The gap:** For infrastructure-heavy enterprises (FSI, telco), software change is a small slice of total change surface. No clear roadmap story or positioning answer for non-software change detection.

---

### Gap #4: ServiceNow + Moogsoft integration — deal blocker at FSI
Both TIAA calls flagged this as a non-negotiable:

> _"ServiceNow integration is a must have. I don't think you — what I'm hearing is you're not a part of the ServiceNow approved list of vendors in the marketplace."_ — **TIAA**

> _"I think you don't have a Moogsoft connector, you don't integrate with Moogsoft, which is our current correlation engine."_ — **TIAA**

**The gap:** Absence from the ServiceNow marketplace is a credibility/compliance issue at FSI, not just a technical gap. Needs to be solved or clearly addressed in the pitch as "on roadmap, here's the timeline."

---

### Gap #5: Pricing opacity — "very atypical for us" ⚠️ MEDIUM PRIORITY
Adobe's commercial call flagged this explicitly:

> _"It's a very opaque pricing model compared to what we are accustomed to seeing. There's no opportunity to separate that into a platform cost and a purchasing of tokens cost."_ — **Adobe procurement (S4 negotiation)**

> _"We are accustomed to receiving transparency on what a credit is defined as. That is very vague here — it's defined by work stream units."_

**The gap:** Large enterprise procurement teams compare credits to LLM token pricing from Anthropic/OpenAI/Gemini and find the mapping opaque. Need a clear "1 credit = X human engineer work" translation that survives procurement scrutiny.

---

### Gap #6: Agent controllability / system prompt configurability — POWER USER CHURN RISK
Block/Square's top SRE user articulated this as the key thing blocking wider rollout:

> _"I wanna be able to be like, you know, bang important, always look at runbooks every single time. Don't do this as early as possible, which I've tried to do as much as I can and it doesn't seem normal listening."_ — **Brandon Zimmerman, Block/Square**

> _"If you could just control the system prompt yourself... holy crap, then it will probably start performing on all the ones that BuilderBot performs better on. It'll probably start performing better than BuilderBot."_ — **Brandon Zimmerman**

**The gap:** Power users at technically sophisticated customers (Block, Adobe) want tenant-level system prompt configuration. Without it, they compare Resolve unfavorably to internal tools ("BuilderBot"). This is a retention/expansion risk for S3-S4 accounts.

---

### Gap #7: Context persistence across chat sessions
Adobe POC and DoorDash both asked about cross-session context sharing:

> _"Does my chat have context from Bogdan's? Like he, maybe he's asking something related to the same problem and Resolve can use the investigation from his chat in order to help me too."_ — **Darius, Adobe POC**

**Resolve's answer:** "It would be fresh. It would be fresh..."

**The gap:** This is a collaboration/team learning question. Prospects expect a shared, team-level memory model. The answer ("use the same thread URL" or "add it to Resolve.md") is technically correct but feels like a workaround.

---

### Gap #8: Database-specific RCA — documented deal loss
PicPay (S3 POC → LOST) gave a clear reason for their exit:

> _"It never gave us a root cause related to database... The max that we had was like, oh, you have slow queries investigate that, but this is what we both have. It's not a great find."_ — **Daniel Reis, PicPay**

> _"Even in some cases that the root cause was simple — the developer was able to find the root cause before the tool for the simple ones, and for the complex ones it didn't get the root cause."_ — **PicPay**

> _"Sometimes it gets better answers than Resolve, even without having the team separated, but it has access to our Confluence via MCP."_ — **PicPay** _(comparing Resolve to their internal tool)_

**The gap:** Database observability (AWS Performance Insights, slow query logs) is a known weakness. PicPay's environment was DB-centric and Resolve couldn't differentiate. This needs either a product gap acknowledgment in qualification, or a "DB observability" integration roadmap.

---

## 6. COMPETITIVE LANDSCAPE (From Prospect Mouths)

| Competitor | What Prospects Said | Context |
|---|---|---|
| **Splunk** | "Now Splunk is doing things you guys are doing. There are a number of others." | HSBC (Petek Ergul). Splunk is the most-mentioned incumbent. |
| **Datadog / Dynatrace** | "The Splunk agent, the Datadog agent, the Dynatrace agent — all these agents are partially blind because they can only look at that part of your stack." | Vasi framing Resolve vs. point solutions |
| **Moogsoft** | "Our event correlation engine is Moogsoft. You don't have a Moogsoft connector." | TIAA — a deal gating issue |
| **ServiceNow** | "ServiceNow might have a light assistant but it doesn't pull in telemetry data, it doesn't pull in code." | Used by Resolve as a contrast point — but also a gating integration requirement |
| **Internal AI / Build-Your-Own** | "Sometimes it gets better answers than Resolve." / "We usually build things like this in house because of the security bar." | PicPay (lost), ADT, HSBC |
| **Cursor / Claude Code** | "So Resolve.md, think of it like Claude.md but for your team." | Adobe — used as an analogy, not competition |
| **Coding Agents (general)** | "If you're autonomously generating a lot of code, doesn't it stand to reason those agents can figure out the production piece too?" | ADT — strategic threat question |

---

## 7. SYNTHESIS: TOP 3 POSITIONING ADJUSTMENTS

### 1. Lead with the "bridge call" story, not "MTTR"
"Reducing MTTR" is generic. "Eliminating the 20-engineer bridge call where 15 people are waiting to hear it's not their team" is visceral, specific, and human. This is the ICP's lived nightmare and Resolve's most differentiated outcome.

### 2. Build a crisp "build vs. buy" response
Every enterprise S1 call raises this. Current answer is hand-wavy. Need: (a) specific TCO of building comparable in-house, (b) production data quality story only available after 12+ months of training, (c) "you're not in the business of building SRE AI." This is the difference between S1→S2 conversion and stalls.

### 3. Address the "reactive-only" positioning gap proactively
Current framing ("we only investigate when triggered, by choice") is losing points with prospects who want proactive AIOps. Either: (a) build a proactive anomaly detection message for the roadmap, or (b) explicitly segment who Resolve is NOT for ("if you need proactive anomaly detection, Dynatrace is your tool — we solve the 'what happened and why' problem they can't solve"). Right now we're leaving this ambiguous and losing credibility.

---

_Report generated from 25+ calls analyzed via Attention | Period: Feb 2 – Apr 2, 2026_
_Accounts covered: LBG, HSBC, TIAA, McKinsey, Adobe (multiple teams), DoorDash, Block/Square, ADT, Invisible, Upgrade, Bloom Credit (Closed Won), Salesforce_
