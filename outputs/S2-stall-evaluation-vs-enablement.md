# Will This Enablement Package Actually Move Deals to S2?

**An evidence-based evaluation of the S1 Discovery Deck + Talk Track + Discovery Questions against real stalled deals from the last 2 months**

Source: Attention call transcripts (Feb 14 - Apr 14, 2026), SFDC opportunity data, 2,055-call sales effectiveness analysis. Accounts analyzed: United Airlines, Wells Fargo, MGM Resorts, Vonage, HubSpot, S&P Global, Ally Financial, Dropbox.

---

## The Honest Answer: It Closes ~60% of the Gap. The Other 40% Needs New Work.

The S1 enablement package is strong on the problems it was designed to solve: inconsistent discovery, missing customer stories, and weak demo narration. But when I stress-tested it against every stalled deal in the last 2 months, three categories of stall emerged that the current package doesn't address at all, and two more where the materials exist but the execution guidance isn't sharp enough to change behavior.

---

## Pattern-by-Pattern Evaluation

### STALL #1: "Incumbent is the default objection"
**The verbatim from Nathan Gray at Ally:** *"Since we already have PagerDuty and Dynatrace, and both have AI SRE products, it would be months faster to get approval on an existing vendor."*

**What the deck does:** The "Resolve Full Stack Differentiation" slide (slide 10) shows post-trained models, multi-agent, continuous improvement, memory system. These are real differentiators. The Coinbase case study (slide 11) provides proof.

**What the talk track does:** The appendix section on "Why is this such a hard AI problem" walks through 5 barriers. The build-vs-buy framing is solid: "You can get to 50% accuracy pretty quickly... the problem is the remaining 50%."

**What the Objection Handling Playbook does:** Slot #1 addresses incumbent overlap with "3-bullet differentiation that every rep can deliver cold."

**VERDICT: 70% covered.** The differentiation content exists, but it's framed as build-vs-buy, not "why not just turn on PagerDuty's AI features." Those are different objections. Nathan isn't saying "we'll build our own" -- he's saying "we already pay for this vendor and they claim to do the same thing." The rebuttal needs to be: here's specifically what Datadog Bits AI / PagerDuty AIOps / Dynatrace Davis does, here's where it stops, and here's the evidence from customers who tried that path first.

**GAP: Need a competitive differentiation one-pager** -- not build-vs-buy, but "incumbent AI features vs. purpose-built AI for prod." Specific to PagerDuty, Datadog, Dynatrace, and Splunk AI.

---

### STALL #2: "Prospects are exploring, not solving"
**The verbatim from Prasanth at Wells Fargo:** *"I'm just trying to understand the technology landscape."*

**What the deck does:** The "Engineering velocity is at risk" slide (slide 3) creates urgency with the AI-for-code vs. AI-for-prod gap. The three pain pillars (slides 4-7) make it visceral. Customer quotes from HSBC, Veeva, and Ticketmaster add emotional weight.

**What the talk track does:** The pre-slide opener is specifically designed for this -- it asks about AI velocity, surfaces the gap, then bridges to "the same three things." The discovery questions are designed to convert exploration into problem identification.

**What the Discovery Question Template does:** "Walk me through a SEV1 step by step" and "When a senior engineer leaves, what happens to that knowledge?" are both designed to surface pain even when the prospect doesn't think they have a specific problem.

**VERDICT: 85% covered -- but reps aren't executing it.** The Wells Fargo call proves the materials exist but weren't used. Prasanth said he was exploring, and Nick moved straight to a technical demo without running discovery. The talk track opener was never deployed. No customer stories were shared. No urgency was created. The problem isn't the content -- it's that reps skip it under time pressure or when the prospect sounds interested.

**GAP: Not a content gap -- an enforcement gap.** The Apr 30 enablement session needs to explicitly drill the opener sequence and make it non-negotiable. Consider a "first 10 minutes" script card that reps keep on their desk. Also: the deck has no "cost of inaction" quantification slide. Adding a simple war-room math calculation (MTTR x engineer cost x incident frequency = annual cost) would give reps a number to anchor urgency for exploring-not-solving accounts.

---

### STALL #3: "Security enters before value lands"
**The verbatim from Chris Hodges at Dropbox:** *"One of the biggest factors slowing AI rollout is compliance, legal, privacy."*

**Wells Fargo proof:** Prasanth spent the majority of the call on deployment models, data residency, and compliance. The value proposition barely got airtime. His literal questions: "Where is the compute plane?", "Where is your cloud?", "Can we run in Google Cloud?", "What about data redaction?" -- all before any discussion of pain or ROI.

**What the deck does:** The "Next Steps" slide (slide 13) mentions satellite deployment and security review, but it's the last content slide. It's not front-loaded. There is no slide that proactively says "here's how this works in regulated environments."

**What the talk track does:** It says: "If asked about data security, mention satellite deployment." That's reactive, not proactive. For healthcare (Personify Health), financial services (Wells Fargo, Ally), and enterprise (Dropbox) -- security isn't something they ask about. It's something that kills the deal before anyone asks.

**What the Objection Handling Playbook does:** Slot #2 says "Lead with satellite, address before they raise it." This is the right instinct but there's no slide or leave-behind to support it.

**VERDICT: 40% covered.** This is one of the biggest gaps. For regulated industries (which are a huge chunk of the pipeline -- Wells Fargo, United, AIG, JPMC, Ally, Broadview FCU), security isn't an objection. It's a prerequisite. If the rep doesn't proactively establish deployment model and data handling in the first 5 minutes, the prospect spends the whole call on security theater instead of value discovery.

**GAP: Need a "Security & Deployment" appendix slide** that reps pull into the main deck for regulated prospects. Content: satellite deployment visual, data handling model (read-only API access, data stays in VPC, redaction), compliance certs (SOC 2 Type II), customer proof (JPMC, BlackRock). Also need a 1-page security brief PDF that can be sent pre-call to accelerate the NDA/security review process. The talk track should add a conditional: "For regulated industries, show this slide immediately after the intro before any discovery."

---

### STALL #4: "No exec sponsor identified"
**The verbatim from Prasanth at Wells Fargo:** *"Nobody owns it -- I just started to look into that area."*

**United proof:** David Gates named Ramiro Zavala (MD) as the budget holder. Jason asked for the name but never pushed for exec engagement. Three months later, no exec meeting has happened.

**MGM proof:** Maneesh reports to Brant, who said "bring these innovative ideas in the later half of the year." Nick never asked to get Brant on a call. The deal is stuck waiting for Maneesh to champion internally.

**What the deck does:** Nothing. The deck is designed for the technical champion. There is no content designed to help that champion sell up.

**What the talk track does:** The closing question "Who else should be in the room for the deep-dive?" is good. The coaching note about the SRE trap is excellent. But it's at the end of the call -- by then the meeting is wrapping up and it's too late to pivot.

**What the Discovery Question Template does:** Question #5 addresses multi-threading. Good.

**VERDICT: 50% covered.** The discovery question and coaching note are right, but the execution data shows reps ask the question politely and accept vague answers ("I'll check internally"). The deck has zero content designed for executive audiences -- no ROI slide, no business case framework, no "why your VP should care" framing.

**GAP: Need two things.** (1) A "champion enablement kit" -- a 1-page internal pitch document the champion can forward to their VP/CIO. Should include: 3-bullet pain summary, Coinbase ROI proof, "what a 4-week pilot looks like," and a calendar link. (2) The talk track needs the multi-threading question moved earlier -- not in the close, but during the pain pillar discussion: "Who owns the budget for reliability tooling? And is that the same person who feels this pain?" This surfaces the org map before the call ends.

---

### STALL #5: "Migration timing = explicit deferral"
**The verbatim from Maneesh at MGM (quoting his boss Brant):** *"Why don't we bring these innovative ideas in the later half of the year."*

**MGM proof:** Kubernetes migration won't have real workloads until June-July 2026. Brant explicitly deferred. Maneesh wants to engage but can't override his manager's timeline.

**United proof:** Just finished a 30-year mainframe migration. David Gates said they were "driving in six different directions." Timeline pushed to "week of March 9th" for first regular sync.

**Wells Fargo proof:** OCP migration and data center migration in progress. Prasanth framed the engagement as exploratory because of competing initiatives.

**What the deck does:** Nothing addresses timing objections or competing priorities.

**What the talk track does:** Nothing. No talk track section for "we're not ready yet."

**What the Objection Handling Playbook does:** Nothing. There's no scripted response for "come back next quarter/half."

**What the Discovery Question Template does:** No question about competing initiatives or migration timelines.

**VERDICT: 0% covered. This is the single biggest gap in the enablement package.** Migration timing is the #5 stall pattern from the 28-account analysis, but it might be the hardest to overcome because it's not an objection -- it's a legitimate business constraint. The prospect isn't saying "no," they're saying "not now," and the rep has no response other than "sure, we'll follow up later."

**GAP: Need three things.** (1) A talk track section: "Why deploying during a migration is actually the best time" -- frame it as: Resolve learns your environment as it changes, so deploying alongside a migration means the knowledge graph builds context on the new architecture from day one. Waiting means you deploy after migration and have to teach the system retroactively. (2) A discovery question: "What's the biggest operational risk during your migration? If a SEV1 hits during cutover, what's your plan?" -- this creates urgency by highlighting that migration periods are the highest-risk time for incidents. (3) An objection response in the playbook: "We actually prefer to start during transitions. At Coinbase, they started during a major K8s expansion and the system learned their architecture as it evolved. The alternative is deploying after stabilization and having to retroactively teach the system what you already went through."

---

### STALL #6: "POC requests lack scope or exec"
**The verbatim from Kartik at HubSpot (paraphrased by Mahir):** *"Kartik is hiring someone to manage that process, who's starting in a couple of months."*

**HubSpot proof:** There was "impetus to try to build something somewhat similar to Resolve internally." The deal is stuck between build-vs-buy and an unscoped POC with no exec sponsor. Someone is literally being hired to figure this out in "a couple of months."

**Vonage proof:** Anil said "Let me run it with my manager to say, with all the investment done in Glean and all the budget related discussions we are having, next step at least should we do a POV or not?" Rep accepted this and offered to send materials. No scope defined, no exec engaged.

**What the deck does:** The "Next Steps" slide lists 4 generic steps. Step 2 says "Identify owners" which is close but doesn't define success criteria or exec involvement.

**What the talk track does:** Says "lock down 2-3 use cases" and "define success criteria together." The framing is right.

**What the Discovery Question Template does:** "Of incidents, alert triage, and production debugging -- which moves the needle most?" helps scope.

**VERDICT: 55% covered.** The talk track and discovery questions help scope the POC, but neither addresses the exec buy-in problem. The current "Next Steps" slide is passive -- it asks the prospect to "identify owners" without creating urgency or structure. The rep is left hoping the champion follows through.

**GAP: Need a structured "Path to Pilot" one-pager** to share at the end of every S1 call. Content: (1) 3 specific use cases to validate (selected during discovery), (2) success criteria template (what good looks like in 4 weeks), (3) required participants (technical team + exec sponsor), (4) timeline (2-week shadow mode, 2-week active). Also: the "Next Steps" slide should be reframed from 4 generic boxes to a specific pilot timeline visual -- "Here's what the next 30 days look like" -- that creates momentum and makes the prospect feel like something concrete is happening.

---

### STALL #7: "Demo isn't arming the champion"
**The verbatim from Nathan Gray at Ally:** *"I'm excited about Resolve but everyone else was like, yeah, this seems like what everyone else says they do."*

**What the deck does:** Coinbase case study (slide 11) is strong proof -- 72% investigation time cut, organic adoption, "gets work done 95% of the time." But this is Resolve's story, not the champion's story to retell.

**What the talk track does:** Excellent demo narration guidance -- "see how every claim has a citation?" and "notice this -- Resolve isn't just taking its first theory." Also has the evidence grounding callout and self-critique framing.

**What the Discovery Question Template does:** Not directly relevant.

**VERDICT: 65% covered.** The talk track demo guidance is strong and would help reps narrate differentiation better. The Coinbase story is compelling. But the champion can't take the talk track home. After the call ends, Nathan goes back to his team and says "it was cool" -- and his team says "so does everyone else." He needs ammunition to re-sell.

**GAP: Need a "champion leave-behind" document.** A 1-page PDF the champion can forward after the demo. Content: (1) "What makes Resolve different from turning on your existing vendor's AI" -- 3 specific technical differentiators with evidence, (2) Coinbase before/after in 2 sentences, (3) "What a pilot would look like for [their company]" -- customized based on discovery. This is the document that Nathan forwards to his team that answers "this seems like what everyone else says they do." The talk track should instruct reps to explicitly say: "I'm going to send you a one-pager after this call that you can forward to your team. It covers exactly why this is different from what you'd get from PagerDuty or Datadog."

---

## Summary Scorecard

| Stall Pattern | Deck | Talk Track | Discovery Qs | Objection Playbook | Overall Coverage |
|---|---|---|---|---|---|
| #1 Incumbent is default | Partial (tech diff) | Good (build-vs-buy) | None | Good | **70%** |
| #2 Exploring, not solving | Good (urgency slides) | Excellent (opener) | Excellent | N/A | **85%** |
| #3 Security before value | Weak (end of deck) | Reactive only | None | Partial | **40%** |
| #4 No exec sponsor | None | Partial (closing Q) | Good (#5) | None | **50%** |
| #5 Migration timing | None | None | None | None | **0%** |
| #6 POC lacks scope/exec | Weak (generic) | Partial | Good | None | **55%** |
| #7 Demo not arming champion | Good (Coinbase) | Excellent (narration) | N/A | N/A | **65%** |

**Weighted average (by deal frequency): ~58% coverage**

---

## The 5 Deliverables That Would Close the Remaining 40%

### 1. Competitive Differentiation One-Pager (addresses Stall #1)
Not build-vs-buy. Specifically: "Your existing vendor added AI features. Here's why that's not the same thing." Cover PagerDuty AIOps, Datadog Bits AI, Dynatrace Davis, BigPanda. Side-by-side: what they do vs. what purpose-built AI for prod does. Evidence from customers who tried the incumbent path first (AIG's Paolo: "I can feed my tickets to Claude Code and do the same thing" -- and what the actual rebuttal is).

### 2. Security & Deployment Pre-Brief (addresses Stall #3)
A 1-page PDF sent before the first call to regulated prospects. Content: satellite deployment architecture, data handling model, compliance certs, regulated customer logos. Goal: take security off the table before the call so discovery can focus on pain and value. Also: an appendix slide for the deck to use conditionally.

### 3. "Why Now, Even During a Migration" Talk Track Module (addresses Stall #5)
A new section in the talk track and objection playbook. Key frame: migrations are the highest-risk time for incidents and the best time to build AI context. Coinbase proof (started during K8s expansion). Discovery question: "What's your plan if a SEV1 hits during cutover?" Objection response for "come back later."

### 4. Champion Enablement Kit (addresses Stalls #4 and #7)
A leave-behind package the champion can forward internally. Contains: (a) 1-page executive summary ("why your VP should take this meeting"), (b) 3-bullet differentiation that answers "this seems like what everyone else does," (c) Coinbase before/after, (d) "what a 4-week pilot looks like," (e) calendar link for the deep-dive. The talk track should instruct reps to explicitly offer this at the end of every S1 call.

### 5. Structured "Path to Pilot" Template (addresses Stall #6)
Replace the generic "Next Steps" slide content with a specific timeline. Share as a 1-pager at end of S1. Content: 3 use cases to validate (filled in from discovery), success criteria, required participants (including exec sponsor), 30-day timeline (week 1-2: shadow mode, week 3-4: active, week 5: results review with exec). This turns "let me check internally" into "here's what we're committing to."

---

## What the Enablement Package Does Well (Keep These)

The evaluation isn't all gaps. Several elements of the current package are directly validated by the call data:

**The pre-slide opener works when reps use it.** The AI velocity gap question is exactly the right way to start with exploring-not-solving prospects. Prodan's "why" question at Personify Health proved how powerful follow-up discovery is. The problem is execution, not content.

**The tribal knowledge thread is the #1 pain.** The talk track correctly identifies this and the discovery questions lead with it. Every single stalled account in the analysis has some version of this pain: Wells Fargo ("a lot of basically undocumented information in people's heads"), MGM ("we don't know who owns what"), United ("only two engineers who know the system"), Vonage ("taking your smartest engineers and disseminating that knowledge"). The deck's Engineering Leverage slide (slide 7) visualizes this perfectly.

**The Coinbase story is the right proof point.** Every element of the Coinbase narrative maps to a real stall pattern: organic adoption (answers "will my team actually use this?"), 72% investigation time cut (answers "what's the ROI?"), started with shadow mode (answers "is this risky?"). The talk track's narration of this story is strong.

**The "not a black box" differentiator is real.** The 2,055-call analysis showed evidence grounding is the strongest unmarketed capability. The talk track calls it out during the demo. This should survive intact.

**The use case qualification question is critical.** "Of incidents, alert triage, and production debugging -- which moves the needle most?" directly prevents the unfocused POC stall. Keep this as a mandatory question.

---

## Bottom Line

The current enablement package would have meaningfully changed the outcome on 4 of the 7 stall patterns -- if reps execute it consistently. That's real progress. The Apr 30 session should focus on drilling the opener, the tribal knowledge thread, and the closing multi-thread question until they're muscle memory.

But the package has blind spots on three patterns -- migration timing, security pre-emption, and champion enablement -- that no amount of training will fix because the content simply doesn't exist yet. Those three patterns account for roughly 40% of the stalled pipeline. Building the five deliverables above would close that gap.

Recommended priority order for the new deliverables:
1. **Champion Enablement Kit** -- highest ROI, addresses two stall patterns, can be built in a week
2. **"Why Now" Migration Module** -- hardest to create but addresses the biggest zero-coverage gap
3. **Security Pre-Brief** -- straightforward to build, immediate impact on regulated pipeline
4. **Competitive Differentiation One-Pager** -- important but partially covered by existing playbook
5. **Path to Pilot Template** -- partially covered, incremental improvement

---

*Based on Attention call transcripts from United Airlines, Wells Fargo, MGM Resorts, Vonage, HubSpot, Ally Financial, Dropbox, and S&P Global. Cross-referenced with 2,055-call sales effectiveness analysis (Jan-Apr 2026) and S1 Discovery Deck v7, talk track, discovery question template, and objection handling playbook.*
