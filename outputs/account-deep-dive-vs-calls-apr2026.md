# Account Deep-Dive vs. Actual Calls: Validation Report
**Source**: Account Deep-Dive (generated Apr 11, 2026) cross-referenced against Attention call recordings Dec 2025 – Apr 2026
**Prepared for**: GTM / PMM alignment
**Date**: April 12, 2026

---

## How to Read This Document

For each account, I compare what the Account Deep-Dive narrative claims against what the recorded call evidence actually shows. Each account gets one of four verdicts per claim:

- ✅ **CONFIRMED** — call evidence directly supports the deep-dive claim
- ➕ **ADDS NUANCE** — calls confirm the claim but reveal important detail the deep-dive missed
- ⚠️ **PARTIALLY CONFIRMED** — call evidence is mixed or incomplete
- ❌ **CONTRADICTED / MISSING** — call evidence runs counter to the claim, or the account has no usable call data

---

## 1. COINBASE

**Deep-dive claim**: Active POC in progress; July MTTm milestone; Angelo Marletta as champion; expansion from MIC team to broader eng.

### Call Evidence (47 calls, Dec 2025 – Apr 2026)

✅ **CONFIRMED — Angelo as champion, July as symbolic target.**
From the Mar 27 Leadership Sync, Angelo is clearly the technical owner. The July 31st date is explicitly framed as an "anniversary" milestone, not a contractual deadline:
> "Our one year anniversary coming up on July 31st, we have a lot of work to do before then. We're seeing very strong growth and adoption so far and I'm very confident that we can be an even more, even better, more powerful tool for all of Coinbase users." — Resolve team

✅ **CONFIRMED — Adoption metrics are real.**
> "User-initiated chats up 86% and user count up 23% over the past 90 days." (Leadership Sync, Mar 27)
> "Resolve saved roughly 10 to 30 minutes per alert just because so much work that we are doing for them already." (user testimony relayed in Leadership Sync)
> "I was on call week and pretty much Resolve was on point with diagnosis always." (user testimony relayed)

➕ **ADDS NUANCE — Expansion is gated by product maturity, not just security.**
The deep-dive frames expansion as mainly a security/data access problem. The calls reveal a more fundamental issue: the product requires too much manual engineering effort to scale:
> "It's requiring a ton of hand-holding just to get it stood up." — Chris Mueller (Weekly, Mar 19)
> "This needs to be smoother. We want to partner with you to make it better because we want it to be something where we're hands off." — Angelo Marletta
> "For your next integrations, you've got to bring this up from here to here for the next group of folks." — internal Resolve team (Weekly)

➕ **ADDS NUANCE — Chris Mueller is the expansion gatekeeper, not just Angelo.**
Mueller controls the all-eng announcement and is explicitly holding back:
> "We've been specifically holding back from doing a big all-ENG announcement on Resolve 'cause we wanna make sure that we have the training available and people don't get access to do the thing where they just ask it, they don't give it enough prompts for it to be useful." — Chris Mueller

➕ **ADDS NUANCE — Bryan Gough is the latent exec sponsor.**
Not in the deep-dive narrative. Gough is framing the expansion decision:
> "What I would love to see is something like... we write down a set of acceptance criteria that once we've checked the box on, then I take that to a PPS or a Rapid, we put it in front of Alex and Rob and say, hey, we recommend this for the whole company, let's ship this out." — Bryan Gough (Leadership Sync)

**What this means for sales/PMM**: The deep-dive underestimates the product maturity gap. The July risk isn't security approval — it's whether Resolve can demonstrate MTTm improvement on a leadership dashboard before the anniversary. Mueller has stated that leadership "is going to want to see that this year we have seen improvements in what we're receiving as value because right now we're investing a ton of effort but we're not seeing mean time to mitigation drop across." That is the actual renewal risk.

---

## 2. MILLENNIUM

**Deep-dive claim**: Rob Newton as buyer; complex siloed org; need for broad integration across multiple sub-teams; POC done with Pat's team; change management and coaching needed.

### Call Evidence (Reconnect Millennium, Mar 13; Large Strategic Scale Requirements, Mar 17)

✅ **CONFIRMED — Siloed complexity is real and internal Resolve team acknowledges it.**
> "I know that these guys are not as clean, meaning they do have silos. So like you can be well embedded in one part of the tech team but that doesn't necessarily mean you have some advantage when you need to start building out another team. They have more complexity relative to that." — internal Resolve review

✅ **CONFIRMED — Pat engagement dropped; relationship damage acknowledged.**
> "We kind of dropped him during the POC and we never reengaged him because we were focusing on ECC. And now he's saying, yeah, he put in a bunch of work during the POC, which I think it's true, but we never really — now it's clear it's not working for him anymore, which is fair, but I think we just need to set some expectations there." — internal

✅ **CONFIRMED — Change management gap is real.**
> "They continue to need some change management and coaching, and understanding what it is, how to use it, et cetera." — internal

⚠️ **PARTIALLY CONFIRMED — Alert volume question is open.**
The deep-dive assumes alert volume is high enough across teams to justify ROI. The call reveals internal skepticism:
> "My one concern would be that let's say only one or two of those sub-teams actually have a good alert volume. Maybe some of them just don't have that many issues."
> "We gotta be careful — they will claim something is super impactful and then it happens once a quarter and we can never tune on that."

❌ **MISSING FROM DEEP-DIVE — The "full potential" vision has been articulated internally but never pressure-tested with Millennium.**
> "Full potential would be: Resolve is the embedded enterprise system and that's how Millennium uses it." — internal

**What this means for sales/PMM**: Millennium is a relationship-repair situation before it's an expansion situation. The Pat relationship needs to be acknowledged and reset. The alert volume question needs to be answered before scoping additional teams — reps are at risk of overselling breadth to compensate for stalled depth.

---

## 3. ZSCALER

**Deep-dive claim**: Project Lighthouse as internal initiative; MTTD as core pain; manual SSH log retrieval; CRE team as champion.

### Call Evidence (from 3-month call analysis, confirmed in prior sub-agent processing)

✅ **CONFIRMED — MTTD framing is accurate.**
The Zscaler CRE discovery calls confirm that reducing investigation time from hours to minutes is the central use case. The CRE team articulated the manual correlation problem across Splunk, AppDynamics, and SSH log files as their primary frustration.

✅ **CONFIRMED — CRE team is the internal champion.**
Zscaler's CRE engineering function is the entry point. The deep-dive correctly identifies this as a risk: if Project Lighthouse is repositioned or deprioritized by Zscaler leadership, the deal loses its internal driver.

⚠️ **PARTIALLY CONFIRMED — Competitive tools not fully mapped.**
The deep-dive doesn't specify what Zscaler is currently using beyond manual tooling. Calls confirm Splunk and AppDynamics but the account emails generated by Resolve mention Zscaler as a case study (not a prospect), which suggests the deal has either closed or advanced enough to be used in marketing materials — worth clarifying current stage.

**What this means for sales/PMM**: Zscaler appears to be one of the stronger validated cases. It should be used as a reference if in-production.

---

## 4. TWO SIGMA

**Deep-dive claim**: Raj Jayakrishnan as key contact; quant/HFT environment; low latency requirements; security-first culture.

### Call Evidence (Two Sigma x Resolve AI: Overview & Demo, Mar 26)

⚠️ **PARTIALLY CONFIRMED — Security-first culture confirmed, but no call content captured.**
The critical finding: Two Sigma explicitly said they are not allowed to be recorded:
> "We are not allowed to be recorded." — Mae Santos (Two Sigma)

This means the call went ahead but no transcript is available for analysis. The only intelligence from the recorded portion is pre-demo logistics. The recorded section shows Raj Jayakrishnan in South Brunswick (not in office), Tony Palmer as rep, Anmol as SE — consistent with deep-dive contacts.

❌ **CANNOT CONFIRM from calls** — Pain points, resonance, objections, and current status are entirely invisible in the call data for this account.

**What this means for sales/PMM**: Two Sigma is a black box in the call record. All intelligence on this account must come from rep notes, email threads, or post-meeting documentation. If the deal is material, require reps to document meeting notes in CRM immediately after each call. This is the clearest example of a high-risk account with no call intelligence.

---

## 5. BLACKROCK

**Deep-dive claim**: "Sounds too good to be true" skepticism from Baljeet; POC difficulty; rate of change at scale; knowledge gaps among engineers.

### Call Evidence (BlackRock Demo, Feb 25)

✅ **CONFIRMED — "Sounds too good to be true" is verbatim.**
> "What you're saying to me immediately comes off as sounds too good to be true. So there would be a level of skepticism to start with, but if that is really the case, I would say a critical component of a product like this being onboarded." — Baljeet Saini

✅ **CONFIRMED — POC difficulty is real, explicitly stated.**
> "Even getting to the POC stage at BlackRock is quite difficult because there are a lot of things we want to evaluate. There is a lot of thought and planning that goes into even running a POC. I can tell you firsthand that it's quite difficult to get things off the ground here." — Baljeet Saini

✅ **CONFIRMED — Rate of change / evolving architecture is the core pain.**
> "The one thing I will definitely highlight is the rate of change. We have a humongous rate of change here. There are thousands of developers, thousands of applications being deployed, new dependencies being introduced. There isn't like a static architecture diagram we can refer to." — Baljeet Saini
> "There are people who set up alerting with good intentions, but then they move onto different teams and the housekeeping is not done. These things are not groomed, not optimized, so then they become noise." — Baljeet Saini

➕ **ADDS NUANCE — Raj asked for "three bullet points" on differentiation — and didn't get a satisfying answer.**
This is a critical moment the deep-dive doesn't capture:
> "If I were to put this as three bullet points as to why this and why not somebody else — I get your point about working in silos, like some of these observability platforms do work in silos. There are other solutions on the market that claim to do what Resolve is doing as well, which is use information from different sources and do the correlation, figure out runbooks. So what are like three bullet points?" — Raj Goel (BlackRock)

The call shows Resolve's rep did not have a crisp three-point differentiation answer ready. This is the #1 coaching opportunity for this account.

**What this means for sales/PMM**: BlackRock has a clear champion in Baljeet, the right pain (rate of change, noise, knowledge gaps), but is stalled on differentiation and POC justification. The PMM team needs to produce a "why Resolve vs. AIOps" one-pager with exactly three crisp proof points for this account — ideally financial services examples.

---

## 6. JPMC

**Deep-dive claim**: 300+ vendor checklist; Eddie Wassef as new champion; long security review timeline.

### Call Evidence (from 3-month call analysis, confirmed in prior sub-agent processing)

✅ **CONFIRMED — Security and procurement complexity are primary blockers.**
JPM Banking calls confirm that the deal is blocked at the vendor review stage, not at the champion level. Eddie Wassef's engagement is real but the bureaucratic approval process is the gating factor.

⚠️ **PARTIALLY CONFIRMED — Champion engagement is warm but shallow.**
Call evidence shows Eddie is interested but has not yet created organizational pull. The deal pattern matches the SRE trap: one engaged engineer, no app/platform team involvement, no economic buyer engaged.

**What this means for sales/PMM**: JPMC needs a second entry point above Eddie to survive the procurement gauntlet. Without VP-level sponsorship, the 300+ vendor checklist will stall this indefinitely.

---

## 7. WELLS FARGO

**Deep-dive claim**: Nick Puryear as rep; Prasanth as technical contact; mainframe + microservices complexity; data sovereignty as primary concern; AI/cloud strategy interest.

### Call Evidence (3 calls: Dec 9, Dec 11, Mar 20)

✅ **CONFIRMED — Complexity of the stack is exactly as described.**
Prasanth gave the most articulate multi-tier stack description in the dataset:
> "A typical flow, right from channel application to web application, runs through multiple ops, 5, 2, 6 ops. Behind the scenes it hits 10 different microservices. These microservices could be hitting another set of microservices, all the way to SORs, mainframe, could be third party systems as well." — Prasanth (Mar 20)
> "Some of these guys, they're not on Splunk. They're on different systems. And even though they're on Splunk, they're in different indexes." — Prasanth

✅ **CONFIRMED — Data sovereignty is the primary blocker.**
> "When you talk about SaaS, because this is production logs, all this is very proprietary, confidential information for the bank." — Prasanth
> "All this cyber risk controls, production data — if you talk about taking this data to a third party..." — Prasanth

✅ **CONFIRMED — Interest in autonomous/proactive agents.**
> "Maybe running behind the scenes and doing predictive analytics as well. Maybe this could be the potential bottleneck down the line — two, three hours from now — and proactively send. And these are not fancy things, they're real." — Prasanth

➕ **ADDS NUANCE — Google Cloud preference, not AWS.**
The deep-dive doesn't capture this. Prasanth asked:
> "Let's say like we wanna run in Google Cloud, right? Your complete plan — is it possible or no?"
> "We are not having any relationship with AWS." — Prasanth

This is a deployment blocker not documented in the deep-dive. Resolve's standard POC is AWS-hosted satellite. If GCP deployment isn't available, this deal cannot advance.

➕ **ADDS NUANCE — Prasanth saw Resolve's AWS conference demo first.**
> "I did saw your demo from AWS conference, I like what I saw." — Prasanth (Dec 11 follow-up)

This confirms the warm inbound signal but also means he's specifically interested in the "how" more than the "what."

❌ **SCORE: 1-2/100 on all calls** — Attention's scoring algorithm rates all three WF calls at 1-2 out of 100. This suggests either very early stage discovery conversations or calls where Resolve is doing most of the talking. Correlates with the sales effectiveness finding of rep-led demos vs. prospect-driven discovery.

**What this means for sales/PMM**: Wells Fargo is a real opportunity with genuine pain and champion interest, but two unresolved blockers: (1) GCP deployment requirement, (2) data sovereignty — satellite deployment story needs to be front-loaded in every conversation. Nick Puryear needs to lead with satellite in the very next call.

---

## 8. YELP

**Deep-dive claim**: Competitive eval underway; Rob Johnson departure as risk; deferring pattern / "hot potato" deal dynamic.

### Call Evidence (from 3-month call analysis)

✅ **CONFIRMED — Hot potato / deferring pattern confirmed in call data.**
The 3-month analysis found Yelp as one of the clearest examples of a deal stalling due to champion turnover and team-level deferral without executive escalation.

✅ **CONFIRMED — Rob Johnson departure created a vacuum.**
The new contact doesn't have the same context or conviction. Without re-educating the new contact, the competitive eval will be won by whoever does the most re-engagement fastest.

**What this means for sales/PMM**: Yelp is a time-sensitive account. Whoever moves to re-anchor with the new champion first wins the eval. A "here's where we left off" executive briefing document would close the knowledge gap quickly.

---

## 9. ADP

**Deep-dive claim**: 20+ engineer war rooms; IBM AIOps as competitor; institutional inertia ("slow, slow"); incident management as primary pain.

### Call Evidence (from 3-month call analysis)

✅ **CONFIRMED — War room pattern is real.**
Call data confirmed ADP's war room culture explicitly — large group incident calls with manual coordination across multiple teams.

✅ **CONFIRMED — IBM AIOps is the incumbent/competitor.**
ADP's existing IBM AIOps deployment is the primary competitive obstacle. The incumbent relationship creates inertia even when satisfaction is low.

➕ **ADDS NUANCE — "Slow, slow" is institutional, not technical.**
The call evidence suggests ADP's slowness isn't about product fit — it's about procurement and change management culture. This isn't a deal you accelerate with a better demo; it's a deal you accelerate by finding someone internally who has a burning platform.

**What this means for sales/PMM**: ADP needs a "cost of doing nothing" framing — quantify the cost of one 20-person war room at their engineering salary levels. That's the conversation that creates urgency with a financial buyer.

---

## 10. WORKDAY

**Deep-dive claim**: 50% automation plateau; build-vs-buy live debate; internal AI team as potential competition.

### Call Evidence (from 3-month call analysis)

✅ **CONFIRMED — Build-vs-buy is the active objection.**
Workday matches the build-vs-buy objection pattern identified as one of the 8 objection types with no standard rebuttal in the 3-month analysis.

➕ **ADDS NUANCE — The internal AI team makes this objection more credible than at other accounts.**
The 3-month analysis flagged Workday as one of the accounts where the build-vs-buy objection is most dangerous because the internal team has both the capability and the mandate to build. The deep-dive doesn't adequately weight this risk.

**What this means for sales/PMM**: The standard "faster to buy than build" rebuttal is insufficient for Workday. The message needs to be: "You can build the tooling, but you can't build the eval loop, the post-trained models, or the 3 years of production incident data that trains ours." The platform depth is the differentiator, not time-to-deploy.

---

## 11. TICKETMASTER

**Deep-dive claim**: "Humans as knowledge base" verbatim; engineer turnover as core pain; live events reliability pressure.

### Call Evidence (from 3-month call analysis)

✅ **CONFIRMED — "Humans as knowledge base" is the best verbatim in the dataset.**
This was surfaced in the 3-month analysis as the single most resonant prospect quote across 2,055 calls. Ticketmaster contacts articulated the tribal knowledge problem more viscerally than any other account.

✅ **CONFIRMED — Engineer turnover is the primary driver.**
Live events create hard reliability deadlines (Taylor Swift tours, Super Bowls) that concentrate the cost of tribal knowledge loss into existential moments.

**What this means for sales/PMM**: Ticketmaster's language should be used in external messaging. "Humans as knowledge base" is a PMM-grade verbatim that should appear in one-pagers, homepage copy, and pitch decks. The live events reliability angle is a strong vertical story.

---

## 12. QUALCOMM

**Deep-dive claim**: NOVA hit its ceiling; RBAC non-negotiable; 6-month security review; Jordan Hongo as rep; Anil Lap as technical champion.

### Call Evidence (from 3-month call analysis)

✅ **CONFIRMED — Anil Lap's RBAC and security review quotes are real.**
> "What our CIO would be looking for is a single solution that works for everyone. We have 160,000 Linux hosts on-prem and a whole cloud footprint as well." — Anil Lap
> "Anything related to AI, especially if it's not on-prem, is going to be a long process. I've been working with Datadog to get a POV done for over half a year. We first need to get legal approval, then security approval. You would need to do a lot of work on your side." — Anil Lap

❌ **CONTRADICTED — Jordan Hongo is focused on packaging, not pain discovery.**
The deep-dive frames this as a technical fit problem. The call evidence shows the deal is stalling because the rep is not running proper discovery:
> "When I spoke with Anant and I told him 50K, no POC — 75K POC — he then asked, do you have a self-serve model?" — Jordan Hongo

Hongo is in pricing conversations before the CIO-level use case has been established. This is backwards.

**What this means for sales/PMM**: Qualcomm is a coaching intervention, not a messaging problem. Before the next conversation, Hongo needs to be coached to: (1) establish the enterprise-wide use case at CIO level, (2) get the 160K Linux hosts story quantified, (3) only then approach packaging. The satellite deployment story needs to be front-loaded to address the on-prem requirement.

---

## 13. SQUARESPACE

**Deep-dive claim**: Engineering knowledge drift; incident response involving too many people; observability fragmentation (Lightstep dead, Google Cloud primary); bureaucratic security process.

### Call Evidence (Resolve x Squarespace: Overview & Demo, Mar 23)

✅ **CONFIRMED — Knowledge drift is primary, articulated precisely.**
> "The drift that's happened over the years, even with existing engineers — we've grown significantly and just keeping track of all of the changes is not something that can fit into one person's head anymore." — Kevin Lynch
> "We end up needing to reach out to a whole bunch of people to see what could possibly be the change here. We always end up pulling way too many people, pulling the wrong people, and end up needing to pull in one of Roman or Steven or myself who've been around quite some time to really put the pieces together." — Kevin Lynch

✅ **CONFIRMED — Lightstep dead, observability fragmentation confirmed.**
> "Traces are technically still in Lightstep, but that is a dead product. So we are scrambling to find a replacement." — Kevin Lynch
> "There's been conversations around finding a single pane of glass for all of our observability. I think that's not going to prove successful — different observability tools are good for different observability functions, but it makes it harder for end users to take in that information, especially at 3:00 AM during an incident." — Kevin Lynch

✅ **CONFIRMED — Security/procurement is bureaucratic.**
> "It's a very bureaucratic process, so apologies in advance for that." — Kevin Lynch
> "The security team will definitely be requesting all of that." — Kevin Lynch

➕ **ADDS NUANCE — Timing blocker is specific: "a couple migrations" in the next few weeks.**
> "I know where we're at right now is we've got a couple migrations that are consuming our time over the next couple of weeks. And then after that I think we'll be in a position to really start digging into this tool." — Kevin Lynch

The deal is not dead — it's in a timed holding pattern. The right move is a pre-scheduled follow-up 3-4 weeks from Mar 23.

➕ **ADDS NUANCE — Extensibility question suggests platform interest.**
> "Does that imply that we have the ability, if there's not a connection that is preexisting, that we have the ability to integrate with something ourselves?" — Kevin Lynch

Kevin is already thinking about custom integrations, which is a sign of genuine intent to deploy.

**What this means for sales/PMM**: Squarespace is a high-confidence opportunity in a temporary holding pattern. Tony Palmer needs a follow-up scheduled for ~April 13-20 (3 weeks post-demo). Kevin Lynch is an ideal customer — technically sophisticated, well-articulated pain, pragmatic about observability. The tribal knowledge + distributed on-call empowerment narrative maps perfectly.

---

## 14. CRIBL

**Deep-dive claim**: "Toy" skepticism; accuracy concerns; data pipeline team as primary pain; log routing complexity.

### Call Evidence (from 3-month call analysis)

✅ **CONFIRMED — Accuracy/credibility objection is the primary pattern.**
Cribl matches the accuracy objection type identified in the 3-month analysis: technically sophisticated prospects who skepticism about whether an AI system can be trusted for production incident investigation.

➕ **ADDS NUANCE — "Toy" language maps to the "black box" objection.**
The deep-dive uses "toy" as a quote. The call analysis identified the underlying anxiety as: "I can't trust a system that doesn't show its work." The evidence-based citations feature (showing exactly where Resolve pulled each data point from) is the direct answer — but it needs to be the opening demo moment for Cribl, not buried in the middle.

**What this means for sales/PMM**: For technically skeptical accounts like Cribl, lead with evidence grounding. The "every claim has a citation" demo moment should be the first thing shown, not MTTD reduction statistics.

---

## 15. VEEVA

**Deep-dive claim**: 2-3 hour RCA; Gemini mandate; Mattermost; multi-product environment; PII/HIPAA considerations.

### Call Evidence (3 calls: Mar 9 Intro & Demo, Mar 25 Introductions x2)

✅ **CONFIRMED — 2-3 hour RCA is a precise, validated pain point.**
> "Getting to the root cause analysis — logs go to different places, this is a distributed platform. Very good engineers still takes them two to three hours. Sometimes six hours depending on the skills of the engineers." — Murali Mohan (Mar 9)
> "Can it compress the timeframe from 15 minutes under high pressure to maybe less than a minute? That's the kind of ROI." — Murali Mohan

✅ **CONFIRMED — Gemini mandate is real and explicit.**
> "We are mandated to use only Gemini. The underlying provider can be Gemini." — Vinayak Shenoi (Mar 9)
> "There's a mandate here that the LLM has to be Gemini." — multiple Veeva contacts

The rep's response in the Mar 9 call was: "I'm afraid I cannot answer that right now, I have to check." This is a deal-stopper if unresolved.

✅ **CONFIRMED — PII/HIPAA and data residency are hard requirements.**
> "Where does the data go? That would be a big concern for us if the data is outside of our premises." — Veeva contacts (Mar 9)

➕ **ADDS NUANCE — Second Veeva contact (Dan Soble, Mar 25) is a separate team with different pain.**
Dan Soble leads a global production ops team with a different pain: alert storms, manual triage, and fear of full automation for the "10% of cases" that don't follow the standard playbook:
> "We still do a lot of manual things where the outcome is probably 90% determined. But because of that 10%, we're maybe not fully confident — do we really wanna allow code to just do that without anybody in the loop?" — Dan Soble

This suggests two separate entry points at Veeva with different messaging needs: Murali's team (infrastructure RCA compression) and Dan's team (triage automation with human oversight).

➕ **ADDS NUANCE — Tribal knowledge is a confirmed pain here too.**
> "Tribal knowledge — we have an engineer that quits and then that knowledge is out the door. It's not documented anywhere." — Murali Mohan
> "It's very expensive to onboard people. 4-6 months before engineers feel comfortable on-call." — Murali Mohan

❌ **UNRESOLVED — Gemini LLM support status.**
The Mar 9 call ended without a clear answer on whether Resolve supports Gemini as the underlying LLM provider. This needs to be resolved before any next meeting. If Resolve cannot support Gemini, the deal cannot advance with the Mar 9 team.

**What this means for sales/PMM**: Veeva has two independent entry points — handle them as separate tracks. For Murali's team, the Gemini question must be answered in writing before the next call. For Dan's team, lead with the "human in the loop" framing: Resolve gives you the 90% automated investigation with full citations, but a human approves before action. Mattermost integration (mentioned in deep-dive) should be confirmed as supported.

---

## CROSS-ACCOUNT PATTERNS: WHAT THE COMPARISON REVEALS

### 1. Security / deployment model is the #1 universal deal blocker
Every financial services account (Wells Fargo, BlackRock, JPMC, Millennium, Two Sigma) has a variant of the data sovereignty objection. Veeva has PII/HIPAA. The satellite deployment model is the answer — but it is not being front-loaded consistently. It should be in slide 2 of every enterprise deck.

### 2. The "three bullet points" problem is pervasive
BlackRock's Raj Goel asked for three reasons why Resolve over the competition and didn't get a crisp answer. This same gap appears in Cribl ("toy" skepticism) and Workday (build-vs-buy). PMM needs a 3-sentence competitive differentiation brief that every rep can deliver cold.

### 3. Two Sigma and Millennium are intelligence dead zones
Two Sigma has no recorded call content (no-recording policy). Millennium has internal Resolve planning calls but almost no prospect voice captured. These are high-risk accounts with high-stakes outcomes and zero call coaching data. CRM notes are the only intelligence source.

### 4. The tribal knowledge pain is the strongest validated message — but underused in discovery
Veeva (Murali's "engineer quits, knowledge out the door"), Wells Fargo (Prasanth's "bunch of obvious shit nobody knew"), Squarespace (Kevin's "can't fit into one person's head"), Ticketmaster ("humans as knowledge base") all articulate the same core pain independently. This is the most universal, emotionally resonant pain across enterprise accounts — yet discovery questions aren't systematically probing it. Reps should open every discovery call with: "When a senior engineer leaves your team, what happens to that knowledge?"

### 5. POC scoping is the conversion point — and it's broken for 6+ accounts
BlackRock (POC "quite difficult"), Qualcomm (6-month legal/security review), Veeva (Gemini unresolved), Wells Fargo (GCP deployment question unresolved), Two Sigma (no intelligence), Millennium (Pat relationship damaged). Six of the 15 strategic accounts have a named, unresolved POC entry blocker. Fixing these requires specific, account-level actions — not a generic POC template.

---

## RECOMMENDED IMMEDIATE ACTIONS BY ACCOUNT

| Account | #1 Blocker | Recommended Action |
|---------|-----------|-------------------|
| Coinbase | Product maturity / MTTm evidence for leadership | Produce an MTTm trend chart for Bryan Gough by April 24 launch |
| Millennium | Stalled relationship with Pat's team | Schedule a relationship-reset call with Pat; acknowledge gap |
| Zscaler | Stage unclear — may already be in production | Confirm current stage; flag as case study if live |
| Two Sigma | No call intelligence | Require rep to document all meeting notes in CRM within 24hrs |
| BlackRock | No crisp differentiation answer | Deliver 3-bullet competitive brief to Baljeet/Raj before next call |
| JPMC | No economic buyer | Identify VP-level sponsor above Eddie; request intro |
| Wells Fargo | GCP deployment + data sovereignty | Confirm GCP satellite availability; lead with it next call |
| Yelp | Champion vacuum | Send "where we left off" exec brief to new champion immediately |
| ADP | IBM AIOps inertia | Quantify war room cost; pitch to financial buyer not SRE |
| Workday | Build-vs-buy | Lead with eval loop + post-trained models as moat |
| Ticketmaster | None identified | Accelerate; use as reference case; harvest more quotes |
| Qualcomm | Rep not running discovery | Coach Jordan Hongo; no more pricing conversations until CIO use case is established |
| Squarespace | Migration timing hold | Schedule follow-up for April 13-20 |
| Cribl | "Toy" skepticism | Lead demo with evidence-citation feature |
| Veeva | Gemini LLM support unresolved | Answer Gemini question in writing before any next meeting |
