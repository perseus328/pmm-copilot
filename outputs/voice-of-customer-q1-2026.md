# Voice of Customer: First Calls & Demos Analysis
**Period:** December 2025 – March 2026
**Calls analyzed:** 25 first calls and demos (Two Sigma, Hidden Road, Alation, Squarespace, Wells Fargo, Yelp, Ticketmaster, Leidos, Cribl, AWS, Veeva, Trading Point, ADP, Workday, Fannie Mae, BlackRock, JFrog, Abridge, Zscaler, JPMC, Asana, Qualcomm, NatWest, Citi, and others)

---

## 1. Key Jobs to Be Done & Customer Pain Points

### 🔴 Pain Point #1: "It takes us 2–4 hours to find root cause — and we're still manually stitching it together"
**MTTR / Incident Investigation Time** — *Universal across all 25 calls*

This is the #1 pain point, raised in every single call. Engineers are spending hours correlating data across siloed tools during incidents, often in multi-person war rooms that are slow and inefficient.

**Soundbites:**
- *"It is the time required to get into the root cause analysis, right? So logs at disparate... there are logs, they go to different places and you have a failure somewhere... Getting into the, okay this is ground zero, this is where the actual term started and then it propagated to the system this year. Very good engineers still takes them two to three hours."* — Murali Mohan, VP Platform Engineering, Veeva
- *"MTTR could be measured in hours or days. Escalations could be a norm."* — SRE Lead, Alation
- *"I remember one incident where it stayed for, you can say more than 24 hours."* — SRE, Alation
- *"We would like to reduce the investigation time, operational talk during incidents."* — Anna Vasileiou, SRE, Trading Point
- *"It takes three to six months for new engineers to get productive because of the complexity."* — Ioannis Mouros, Trading Point
- *"Incidences could result in, you know, war rooms of 20 plus engineers."* — Steve Lovci, Qualcomm
- *"MTTR is always something that management's asking to reduce."* — Steve Lovci, Qualcomm
- *"We respond quite fast and our team operate like 24/7… But we want to make sure there's no downtime in performance. Every second that we are down we are getting a complaint."* — Nicolas Wee, Production Engineer, Hidden Road

---

### 🔴 Pain Point #2: "We can't be setting up alerts for everything — and we don't know what's going to happen before it happens"
**Alert Fatigue & Noisy Signals** — *18 of 25 calls*

Too many alerts that are either noise or not actionable. Engineers develop learned helplessness, ignoring alerts until something causes a major incident.

**Soundbites:**
- *"Noisy alerts is one of the biggest issues in terms of how teams operate their software. And if they properly analyze all of alerts, it will be a full day job to simply answer alerts. At some moment, teams who got too many alerts, simply ignoring alerts... Unless it's causing major incidents and some funds are impacted, it's not an alert."* — Yevhen Zavhorodnii, SRE Lead, Ticketmaster
- *"We don't want to overwhelm our NOC team."* — Engineering Lead, Alation
- *"Each alert takes somewhere between 60 minutes to like two hours, which means that in a week, they're not gonna look at every single alert."* — SRE, Alation
- *"There were actually some precursor signals that... people just don't have enough time to go through and say that alert... But that was the alert that caused an incident where someone could not check out."* — Kevin Lynch, VP Engineering, Squarespace
- *"For me it would be like making or separating the signal from the noise. So we may have a lot of alerting, but using knowledge about the system, figuring out dependencies, correlations, to come up with the probable or the most likely cause..."* — Baljeet, Observability Lead, BlackRock
- *"Multi-tenant alert noise: one root cause could trigger a hundred plus alerts means hours spent triaging manual cross-tool investigation."* — Midhun Mohanan, JFrog
- *"One root cause could trigger alerts for 20 tenants. There is no point looking at all 20 individually."* — Midhun Mohanan, JFrog

---

### 🔴 Pain Point #3: "If that person leaves, the knowledge walks out the door"
**Tribal Knowledge Loss & Knowledge Fragmentation** — *22 of 25 calls*

Knowledge is locked in people's heads, scattered across Confluence/Slack/runbooks, and runbooks are always out of date. This creates risk, slow onboarding, and over-reliance on senior engineers.

**Soundbites:**
- *"Tribal knowledge. So we have an engineer that quits and then, you know, that knowledge is out the door. It's not documented anywhere."* — SRE Lead, Veeva (summarized by Resolve rep)
- *"Documentation is never where it needs to be. There's always emails that are sent out that nobody reads. So it turns into just whenever someone says something factually no longer true, you correct them."* — Kevin Lynch, VP Engineering, Squarespace
- *"We are starting to build custom agents... we tried doing it in-house, but if there's any better tool, yes..."* — Amit Jain, Head of Quant Engineering, Fannie Mae
- *"I would prefer not using human beings as knowledge base."* — Yevhen Zavhorodnii, Ticketmaster
- *"Some reliance on tribal knowledge across the teams, right, how all these systems work."* — Chris Dyer, Engineering Lead, Yelp
- *"Production task requires stitching together knowledge from a variety of different tools... and you know, three or four different people who happen to know something."* — Patrick Chapman, SRE Lead, ADP
- *"There's not one person in the organization who knows how to operate all the tools... That often results in war rooms or people being shoulder tapped and escalations."* — Engineering Lead, Alation
- *"The day-to-day toil... the on-call people not necessarily having the expertise on the system that someone else wrote."* — Ledion Bitincka, CTO, Cribl

---

### 🟠 Pain Point #4: "Our observability is spread out. Each tool has its own silo."
**Multi-Tool Correlation / System Complexity** — *20 of 25 calls*

Customers have 5–10+ observability tools, each with its own data model, access method, and expertise requirement. Getting a cross-tool view requires either manual effort or a human expert.

**Soundbites:**
- *"Diagnosing production issues is difficult because of the complexity of Yelp's system. A single request can fan out across dozens of services, traces become pretty hard to interpret, and then there's a lot of stitching of data across multiple tools."* — Chris Dyer, Yelp
- *"One of the problems that we are seeing is that the AI capabilities are typically restricted to the data that resides in that specific platform."* — Anton Lap, IT Director, Qualcomm
- *"Our observability is kind of spread out. So we have Google for logs and metrics primarily... traces are technically still in Lightstep, but that is a dead product. So we are scrambling."* — Kevin Lynch, Squarespace
- *"One team uses Grafana in one way, the other team uses Grafana in another way. The other team doesn't even use Grafana."* — Vasi Karkantzos (Resolve, summarizing Trading Point's reality)
- *"We are Splunk Enterprise, Splunk Observability, Kibana, AWS Kubernetes, Pagerduty, Fire Hydrant... we have freedom we are giving freedom to other teams to not follow those directions."* — Yevhen Zavhorodnii, Ticketmaster
- *"We have a humongous rate of change here, which understandably by itself sometimes is easy to detect, sometimes hard."* — Raj, Observability Lead, BlackRock

---

### 🟠 Pain Point #5: "We are reactive to a lot of issues. I want to pick these up before they reach the end user."
**Reactive vs. Proactive Operations** — *15 of 25 calls*

Teams know they're stuck in reactive mode and aspire to catch issues before customers do. They want a tool that helps shift left, not just debug faster.

**Soundbites:**
- *"We are reactive to a lot of issues. Like if the client gets affected by an issue, then only then the engineers start looking at it. I was just looking at what are the solutions out there that would help us to try to pick up these issues even before reaching the end users."* — Nicolas Wee, Hidden Road
- *"We want to be able to get to using tools like Resolve to be more proactive where we're observing and we're reacting to issues that are not yet causing customer knowledge."* — SRE Lead, Alation
- *"Maybe running behind the scenes and doing some predictive analytics as well. Maybe this could be the potential bottleneck down the line. Maybe two hours from now and proactively send."* — Prasanth, Distinguished Engineer, Wells Fargo
- *"Have you have any ways to be more proactive in a scenario like that, Hey I noticed this, this is happening every single week. Someone should look at this or here's a potential issue."* — Kevin Lynch, Squarespace
- *"We can never stop development. We can never stop releasing... all the time we are against the clock, we are against pressure and we have to be trying to identify root causes accurately."* — Chris, SRE, Trading Point

---

### 🟠 Pain Point #6: "It's not scale of incidents — it's the scale of information you need to process"
**On-Call Toil, Engineer Burnout & Scaling SRE** — *14 of 25 calls*

Engineers are being paged at 2am for issues outside their expertise, expected to be encyclopedic about complex distributed systems, with no AI augmentation.

**Soundbites:**
- *"The on-call people not necessarily having the expertise on the system that someone else in Europe wrote."* — Ledion Bitincka, CTO, Cribl
- *"People are getting paged at 2:00 AM or like after hours on weekends and like that's something that obviously I'm assuming you're trying to also help alleviate some of this toil."* — Anmol Singh, Resolve (summarizing Squarespace)
- *"Yeah, it's kind of fitting into more, like even some sort of co-pilot for people... when you're jumping into on-call and you have no idea where to start. You just see that something is on fire and you don't even know what is on fire."* — Yevhen Zavhorodnii, Ticketmaster
- *"I know I need to hire SRE #10, I don't want to hire SRE #10. Can you do it for less?"* — Dionysus (Resolve, summarizing customer logic)

---

### 🟡 Pain Point #7 (Emerging): "Security is going to be the biggest barrier to entry for us"
**Security, Compliance & Data Residency** — *All enterprise calls, especially FSI*

This shows up less as a pain point and more as a hard constraint (see Section 2). But it is a job to be done: customers need to evaluate and approve any vendor that touches production telemetry.

---

## 2. Customer Reactions to the Pitch, Objections & Constraints

### Pitch Reactions

**What's generating genuine excitement:**
- The demo moment where Resolve investigates a real incident across multiple tools simultaneously — customers "get it" viscerally
- The knowledge graph / tribal knowledge capture concept
- Automated RCA summaries and postmortems ("It created an incident report, automatically, with the way I wanted it formatted with date and everything")
- The "co-pilot for on-call" framing resonates especially with practitioners

**What's creating hesitation or confusion:**
- The scope and breadth of the pitch can come across as too broad — customers sometimes need to anchor it to their specific environment
- When a non-SRE persona is in the room (Product VP, Business VP), the value doesn't land without translation: *"I'm not a hundred percent clear on what your value proposition is."* — Kunal, Fannie Mae
- The platform is perceived as reactive before proactive — customers want to understand the proactive/predictive story earlier

---

### Objection Map

**🚨 OBJECTION #1 (Universal): Security & Data Residency**
The #1 objection in every enterprise deal, especially FSI (banks, financial services, regulated industries).

- *"This is like production logs... that's all very proprietary, confidential information for the bank, right? All this cyber risk controls."* — Prasanth, Wells Fargo
- *"Any bank or financial... they have the same kind of restrictions that we do, which is you don't exfiltrate your data to SaaS."* — Eddie Wassef, JPMC
- *"We've kind of opted for either an on-prem or a bring-your-own-cloud where we provision you a cloud account that we own."* — Eddie Wassef, JPMC
- *"If we really want to use it, we have to send it through our security tool desk, run through whatever they need to validate."* — Nicolas Wee, Hidden Road
- *"As far as the actual line data environment, we're just waiting for the security team to give us the green light."* — Leidos call

**🚨 OBJECTION #2 (Very Common): "Sounds too good to be true" — AI Accuracy & Trust**
Buyers are skeptical of bold claims after years of AI over-promising, especially in complex, bespoke environments.

- *"What you're saying to me immediately comes off as sounds too good to be true. So there would be a level of skepticism to start with... if that is really the case, that would be a critical component. We understand that the environment that we work in is quite complex."* — Baljeet, BlackRock
- *"What we've seen, and again, a lot of this space is changing fairly quickly, is things not necessarily working as promised in our data or in a customer's environment."* — Ledion Bitincka, CTO, Cribl
- *"When it confidently says here is the root cause... how do you assess and make sure that it's not hallucinating something that we should have ignored?"* — Engineering Lead, Alation
- *"What is the level of confidence that the actual RCA would be useful... or will the agent hallucinate an answer either way?"* — Cristian Iulian Cojocaru, Trading Point

**🟠 OBJECTION #3 (Common): Integration Complexity / "Will it work with our stack?"**
Customers have highly custom, heterogeneous environments. They fear the product only works cleanly on canonical stacks.

- *"Our tech stack is very varied, right? Like it's not — ADP is a big shop. We've got 6,000 developers, multiple business units and almost every business unit is on a separate tech stack."* — Parvinder, ADP
- *"How extendable are those connections? Even if you're covering 90% of the market, given the freedom in our teams, there will be one team that isn't handled."* — Yevhen Zavhorodnii, Ticketmaster
- *"I don't think that would really work for us, given our custom architecture and control plane."* — Engineering lead, Veeva
- *"We do not use Slack in-house. We use a very similar product called Mattermost. Do you have a Mattermost integration?"* — Murali Mohan, Veeva

**🟠 OBJECTION #4 (Common): "What makes you different from [Datadog AI / AWS / existing tools]?"**
Observability vendors are adding AI features. Customers need a crisp competitive differentiation story.

- *"How is this different from all the other solutions in the market? All of the major observability vendors are baking in AI into their tools as well. I'm yet to see what differentiates Resolve from everything else."* — Baljeet, BlackRock
- *"What's the difference of your solution because some of this stuff is already done by AWS also, right?"* — Amit Jain, Fannie Mae
- *"We use Cursor, we use Claude Code. And we have our own AI tooling internally."* — Chaitanya, VP Product, Asana

**🟡 OBJECTION #5 (Situational): Build vs. Buy**
Especially from technically sophisticated companies or those with large internal AI/platform teams.

- *"We are trying doing it in-house, but if there's any better tool, yes."* — Amit Jain, Fannie Mae
- *"If we should actually build the evals framework ourselves, or if we should leverage a partner. We're thinking through what do we build and where do we collaborate."* — Chaitanya, VP Product, Asana
- *"What we've seen, a lot of this space changing fairly quickly, is things not necessarily working as promised."* — Cribl (who makes observability tooling themselves)

**🟡 OBJECTION #6 (Situational): Reactive-Only Perception**
Customers who aspire to proactive operations sometimes initially categorize Resolve as a reactive tool.

- *"I was thinking a little differently in the beginning that it's gonna be embedded in optimizations... but it seemed like this is more reactive to begin with."* — Amit Jain, Fannie Mae

**🟡 OBJECTION #7 (Situational): Wrong Persona in Room / Internal Alignment Needed**
Especially in top-down outbound motions where the right technical decision-maker wasn't present.

- *"I think this is probably for a different audience... we are not in the technology team."* — Lina Gomez, Fannie Mae
- *"I wish Kamran, who's head of infra, was here because he would actually be the right person."* — Chaitanya, VP Product, Asana

---

### Key Constraints

| Constraint | Frequency | Who raises it |
|---|---|---|
| Security review / vendor approval process | Universal | All enterprise, highest in FSI |
| Data residency / no SaaS data exfiltration | Very High | Banks, financial services, government |
| Custom/legacy environment compatibility | High | All large enterprises |
| Centralized identity/access management (SSO, RBAC) | High | Large enterprises (ADP, Wells Fargo, Yelp) |
| Procurement / legal review cycle | Medium | All large enterprises |
| Pricing clarity / ROI justification | Medium | Mid-market and enterprise |
| On-prem or BYO cloud deployment model | High in FSI | JPMC, banks, regulated |
| Integration setup lift (manual, no Terraform/CloudFormation) | Medium | Cloud-heavy customers |

---

## 3. Where the Positioning Lands — and Where it Gaps

### ✅ Positioning That Lands Well

**"An AI SRE that reasons across your entire toolstack"**
The multi-tool correlation angle lands consistently. Customers who are drowning in tool sprawl immediately understand the value prop. The line *"we can reason across different tools in different systems — correlate logs in CloudWatch with logs in Loggly with metrics in Prometheus, and tie that back to code and infrastructure"* resonates. Qualcomm's Anton Lap put it directly: *"AI capabilities are typically restricted to the data that resides in that specific platform. That is something we were trying to solve ourselves."*

**The knowledge / tribal knowledge angle**
The pain is real and deeply felt. When Resolve positions itself as capturing and operationalizing tribal knowledge, customers nod. It's language they use themselves. The Ticketmaster SRE said: *"I would prefer not using human beings as knowledge base."*

**The "co-pilot for on-call" moment**
When the demo shows Resolve being invoked mid-incident and walking through investigation step by step with citations, practitioners light up. Ticketmaster's Yevhen: *"It's kind of a co-pilot for people... when you're jumping into on-call and you have no idea where to start."*

**Proof from peers / naming customers**
Mentioning Coinbase, DoorDash, Salesforce as customers who tried to build this themselves builds credibility. Helps with the build-vs-buy objection.

---

### ⚠️ Positioning Gaps

**GAP #1: "Is this reactive or proactive?" — The pitch doesn't answer this early enough**
Every aspiration-forward customer (Fannie Mae, Hidden Road, Squarespace, Alation) wants proactive / predictive operations, not just faster incident triage. When the demo focuses on incident investigation, some buyers conclude the product is reactive-only. The proactive story (precursor signal detection, proactive health checks) exists but doesn't enter the pitch early enough or clearly enough. Fannie Mae's Amit Jain: *"I was thinking it's going to be embedded in optimizations... but it seemed like this is more reactive."*

**GAP #2: The differentiation story vs. incumbent AI features is weak**
BlackRock's Baljeet articulated the gap precisely: *"How is this different from all the other solutions in the market? Major observability vendors are baking in AI into their tools as well. I'm yet to see what differentiates Resolve from everything else."* There is no tight, repeatable competitive wedge being delivered in first calls. The "we work across all your tools, not just one vendor's" angle is the strongest answer — but it needs to be sharpened into a two-sentence takeaway.

**GAP #3: ICP is landing too broadly — the non-SRE stakeholder gets confused**
When the audience includes business leaders, product managers, or non-technical VPs, the pitch loses them. *"I'm not a hundred percent clear on what your value proposition is"* (Fannie Mae). Resolve needs either different entry-point messaging for different personas, or clearer ICP qualification so non-SRE meetings don't happen at the intro stage.

**GAP #4: Security and deployment model are being handled reactively, not proactively**
Security questions derail late in calls and create unexpected friction. The satellite deployment model, SOC 2, read-only access, no-data-retention story, and BYO-cloud options are strong answers — but they're only surfaced when customers raise concerns. For FSI and regulated industries especially, these should be woven into the standard pitch before the question is asked.

**GAP #5: No clear ROI proof / quantified claims feel unearned**
Customers want numbers, but distrust them. *"If you said 70–80% MTTR reduction, I would say sounds too good to be true"* (BlackRock). The answer is not to stop citing numbers — it's to ground them faster in customer-specific evidence. Customers like Workday and BlackRock explicitly asked: *"Do you have data to point to? Have you measured this?"* Resolve needs proof points with named customers or specific verticals, not just aggregate claims.

**GAP #6: Integration breadth is assumed, not demonstrated**
Customers with Mattermost, non-K8s architectures, legacy Splunk on-prem, or custom control planes worry they'll fall into the 10% Resolve can't cover. The pitch should pre-empt the "what if our stack isn't supported?" objection rather than waiting for it. The custom integration / MCP extensibility story is not breaking through early enough.

**GAP #7: The learning loop / model improvement story is a missed opportunity**
JPMC's Eddie Wassef articulated an untapped value prop: *"If there was a tier where I could opt out, but everybody else — you were training on this error, 80% of your customers handled this error this way — your agent is now an order of magnitude better than your competitor."* Customers want to understand whether the product gets smarter from their environment and from cross-customer patterns. This is a competitive differentiator that's currently not being addressed in the pitch.

---

## Synthesis: Top Recommendations for Messaging

1. **Lead with the proactive story earlier.** The "catch it before customers notice" job is as important as "resolve it faster." The pitch needs to speak to both.

2. **Develop a 2-sentence competitive wedge** vs. Datadog AI, AWS, and internal tools — the multi-tool cross-stack reasoning angle is the differentiator, but it needs to be pre-packaged.

3. **Create a security-first intro slide for FSI.** Security, deployment model (satellite, BYO cloud, SOC 2, read-only, no data retention) should come up before the objection does.

4. **Quantify MTTR improvement with specific customer stories**, not just aggregate percentages. "Customer X reduced MTTR from Y hours to Z minutes in environment type A" will land better than "70–80% improvement."

5. **Sharpen the ICP.** The current pitch works for SRE leads, platform engineers, and engineering directors. It does not work for product VPs, business stakeholders, or engineering leaders at companies that don't yet have a formalized SRE function.

---

*Analysis based on 25 first calls and demos from Dec 2025–Mar 2026 sourced from Attention. Companies represented: Two Sigma, Hidden Road, Alation, Squarespace, Wells Fargo, Yelp, Ticketmaster, Leidos, Cribl, AWS, Veeva, Trading Point, ADP, Workday, Fannie Mae, BlackRock, JFrog, Abridge, Zscaler, JPMC, Asana, Qualcomm, NatWest, Citi, and others.*
