# Resolve AI — PMM Listening Tour: Insights & Action Plan
**Period Analyzed:** March 23 – April 7, 2026
**Meetings Reviewed:** 14 Granola transcripts
**Participants:** Bharath, Vasi, Gary, Jim (Sales Enablement), Brandon, Josh, Victor, Prodan, Brooke (CS), Chris, Varun (Product), Strangefamily (Brand), Anmol (Engineering), Swarit, Daniel
**Prepared by:** Pawan Shankar, PMM

---

## Executive Summary

Two weeks of cross-functional listening reveals Resolve AI is caught between a compelling vision and an inconsistent go-to-market engine. The product wins when the right people test it the right way — but getting there takes too long, costs too many meetings, and relies too heavily on individual heroics rather than a repeatable system. The core problems are four-fold: (1) no shared understanding of what makes Resolve different, (2) a GTM funnel with multiple broken qualification gates, (3) POC methodology that undermines customer confidence, and (4) a post-sales motion that hasn't cracked expansion. This document captures what we've learned and what we need to do about it.

---

## What We Heard: 8 Core Themes

---

### Theme 1: The Funnel Is Broken at Multiple Points

**The signal:** Every seller interviewed, unprompted, mentioned that it takes 15–25 meetings to reach POC. "That's insane," said Vasi. Multiple AEs cited getting stuck between S1 and S3 with no clear forcing function to move forward.

**The root causes:** Three distinct problems compound each other:

**1a. We're stumbling to find the right people.** We enter through whoever we can get to — often a centralized SRE team — and then spend 5–10 meetings trying to triangulate to the application owner, who is the person who actually has code context and can tune Resolve. Gary put it directly: "We're not getting into these conversations as easily as we were in 2025. Cold prospecting in a noisy market is brutal." Brandon added: "We just don't know what we told the customer we can do, so who knows what they're trying."

**1b. Discovery is too shallow at S1.** We're not learning enough in the first call to route customers correctly. We ask the right questions but don't hold the customer to clear qualifying gates before moving forward. Vasi's framework — get a dedicated champion with executive sponsorship and alignment on resources/timing — is working, but it's not universal. "I've never had this conversation with anyone," he said of his methodology. That's the problem.

**1c. Qualification is bleeding into POC.** Brandon's observation: "POC is just becoming another dumping ground for qualification. When that should have been done upfront and early." We're doing discovery work in S3 that should have happened in S1, inflating deal cycles and frustrating customers.

**The gap:** No shared qualifying gates at S1 exit. No documented definition of what "POC-ready" means. AEs are inventing it deal by deal.

---

### Theme 2: Messaging Is Strong in Concept, Broken in Practice

**The signal:** Every person interviewed said some version of "I don't know how to explain what makes us different from DataDog." Gary's quote is the clearest articulation: "We don't have use cases that differentiate us against the market in any way, or we don't talk about our use cases in any way other than the same way that is measured by an AI Ops company."

**The problem in detail:**

The "AI for prod" framing works as a vision — it's category-defining, forward-looking, and true. But when you get to the use cases (alerts, investigations, MTTR reduction), you sound identical to DataDog with AI mode turned on. Brandon said it: "When I start to have Splunk-ish conversations about solving MTTR, we get shoved down to SRE people. And those conversations die."

The brand work with Strangefamily (verbal identity, "Engineering Unbound," the three messaging pillars) is directionally strong. But it hasn't been connected to the product narrative or translated into sales language. Varun acknowledged this live: "The biggest gap I see is that the latest product messaging is purely AI-centric, and I'm not sure how it merges with what we've been building on the brand side."

**What's working upstream:** Thought leadership content (AI SRE guide, AI for prod guide) is actually landing with VPs of Engineering. Gary: "The thought leadership stuff is getting VPs of engineering to the table." But once they arrive, we don't have a crisp story for what's different.

**The differentiator story we're not telling clearly:** Several people named versions of the same thing — the compounding, full-stack approach that gets smarter the more you use it. Gary: "It's like you're investing in Salesforce in 2007." Brandon: "We don't demo our knowledge system. We demo alerts and root cause, which everyone else does." The unique angle — contextual knowledge that compounds over time, cross-stack correlation, and the flywheel effect — is in everyone's head but not in any doc or deck.

---

### Theme 3: ICP Is Ambiguous, and That's Killing Pipeline

**The signal:** When asked "who is our ICP," five different people gave five different answers. Vasi: "The AE doesn't even understand their own portfolio sometimes." Jim: "I don't think we've gritted it out and put the right words in the right boxes."

**The two real archetypes (based on what we've learned):**

**Archetype A — Developer-led, embedded SREs.** Companies like Coinbase, Expedia, Snowflake. Engineering teams own their services. SREs are embedded in app teams. These orgs care deeply about AI tooling, already using Cursor/Claude, and understand the primitives (MCP, MD files, etc.). They move fast and can self-serve once they get the concept. Our risk with them: they'll try to build it themselves.

**Archetype B — Centralized SRE / NOC-style.** Companies like TIA, Zscaler (partially). Centralized ops team handles incidents, but doesn't own the code. Application teams know the code but don't own the alerts. Resolve requires knowledge from the people who own the code, but the SRE team doesn't have it. These deals move slowly because you need two teams to cooperate, and the SRE team often isn't the decision-maker.

**The ICP clarity we need:** Josh: "In a NOC, it's all about predictability. By default they've incorporated a hundred people and their MTTR is through the roof. There's value, but it's a much harder problem." This suggests Archetype A is our primary ICP today and Archetype B requires a longer cycle with more handholding.

**The pendulum swing problem:** Sales swung hard away from SREs ("SREs are a dead end"), which is right in principle, but now we're prospecting to VP/Director-level engineering leaders who don't get the problem — and we have no wedge to open the door with. The answer isn't "not SREs" — it's "get to the EB first, then triangulate to the right application team."

---

### Theme 4: The POC Is Our Biggest Unresolved Debate

**The signal:** Brandon said it flatly: "I don't see a lot working." Prodan: "We're losing because we're not in control of what's being tested in the first place." This is the most heated, politically charged issue in the company right now.

**Two competing POC philosophies:**

**The "tightly scoped" model (current SE-led approach):** Constrain the scope to 2–3 alerts. Set specific success criteria. Prove value on a controlled set. Risk: customers feel we aced our own test. Multiple accounts (Expedia initially, others) reached end of POC and said "that wasn't helpful." Brandon: "We lose a ton of POCs doing it this way."

**The "open scope / prescribe the model" approach (Vasi, Project Perseus):** You prescribe the POC. You don't ask the customer what they want. You show them the plan, get their buy-in, then run it. The success criteria are always the same across deals. Vasi: "90% of the POCs I'm doing have the exact same success criteria. These are prescribed." This approach won Expedia (Project Perseus) and is Vasi's standard model for all his enterprise deals.

**What's actually working in the field:** Vasi's pre-flight document approach:
1. Brainstorm the alert buckets/use cases with customer (S2)
2. Document: challenges, why now, prioritized alert groups, tools needed, team owners, named individuals, roles (user/reviewer/deployer/security)
3. Pre-fill the success scorecard before POC begins
4. Run the "wheel of happiness" — there's no unhappy path: either it works (success) or you find a gap and fix it (also success)

**The expectation-setting problem:** Prodan nailed it: "The product needs to tell the customer when it doesn't know. Right now it tries to answer whether it has context or not." This creates a trust problem when customers see confident-sounding wrong answers. Product gap — but one we can manage through messaging ("Day 1 is college student. Day 100 is PhD. Let's evaluate whether you can close the gap, not whether it's perfect on day 1.").

**The meta-issue:** Brandon: "There's no escalation path for this debate. It just dies." This is a leadership/process gap that Pawan can help bridge — bringing data and a neutral perspective to get alignment.

---

### Theme 5: Post-Sales Has Critical Missing Infrastructure

**The signal:** Brooke (CS/expansion): "We have 15 logos. Most of them are in the 8–12 month window. We have no dashboard. We have no visibility. We don't know what they contracted at. We're not identifying the enterprise buyer early enough."

**The four post-sales gaps:**

**5a. No usage visibility.** Customers don't know how much they're using. We don't know if they're overusing. Coinbase is already 2x over contract — we didn't know until recently. Brooke: "There was no dashboard. We go to customers and say use it more, but they have no idea how much their team is using."

**5b. Wrong buyer at the table.** We land with a team lead at $200–300K. When it's time to expand to $3M+, the guy who signed the original check can't sign. We haven't identified the enterprise buyer — the CTO or CTO-minus-one who actually controls the budget. Brooke: "Has anybody met him? No."

**5c. No structured expansion playbook.** Filippo (AEM on Coinbase) recently built an expansion presentation — but it was from scratch. We don't have a codified expansion motion: what do we present, when, to whom, and how do we use the product usage data to make the case?

**5d. Pricing model confusion mid-cycle.** We moved from $30-per-everything to a credit-based model (35/$10/$0 credits) recently. Customers mid-contract are on old pricing. Coinbase would be paying 10x more under the new model. This creates awkward conversations when trying to expand.

**What's working:** Getting to the senior sponsor and asking them directly to unlock auto-investigations (Millennium). Taking a cab to Salesforce's office after their incident ("don't you need us everywhere now?"). These are the right instincts — opportunistic, relationship-driven expansion moves. But they're ad hoc.

---

### Theme 6: Product Gaps Are Costing Us in the Field

**The signal:** Victor (post-sales SE): "I don't think AI for prod sticks with end users. For engineers, I just say: imagine you hired a person on your team who knows all your systems and tools and is highly coachable."

**The product experience gaps hurting GTM:**

**6a. Too many confusing entry points.** Chat, deep investigation, slash RCA, auto-investigation — four different ways to interact, each with different architectures underneath. Victor: "This is hurting us to some degree. Customers forget to do deep investigation. They don't know slash RCA exists." The solution: the product should decide which mode to use, not the user.

**6b. Knowledge tuning is the biggest lever but customer-facing tooling doesn't support it.** We need customers to write/maintain Resolve MD files, but we give them no feedback loop. Anmol: "We need to build an eval score. We need proposed knowledge that customers approve or reject rather than expecting them to write from scratch." Victor: "A blank page with no idea where to start kills early engagement."

**6c. Integration setup is slow and painful.** Security reviews, Helm charts, config maps — Varun: "These are low-hanging fruit in my opinion. We need an onboarding wizard." Swarit: "Even our own team struggles to get things set up." The self-serve motion doesn't exist yet in any meaningful way.

**6d. The "Resolve as a person" framing is more effective than "AI for prod."** Victor surfaces this unprompted: "When I say 'imagine you hired a new team member who knows your GitHub data, your runbooks, and every tool you use,' people immediately get it. They know how to interact with a person. They don't know what to do with AI for prod." This is a significant messaging insight — the category framing may be right for marketing, but the persona framing closes faster in sales.

---

### Theme 7: Enablement Is Ad Hoc and Going Stale Fast

**The signal:** Jim (Sales Enablement): "It's been almost three months working on the pitch deck certification. It was supposed to be done overnight. The deck changed four times since we started." The market moves faster than any content program can keep up with.

**What exists today:**
- Boot camp: one week for AEs, second week for SEs/AEMs. Run monthly.
- Content: scattered Google Drive folders. "Nobody reads them."
- Win stories: collected ad hoc through Slack, not systematic.
- Competitive: almost none. "We have almost no competitive content," said Jim.
- No knowledge management tool yet (evaluating GTM Buddy, Payflight).

**The systematic problems:**
- No feedback loop from field to PMM. What's landing, what's not — unknown except by anecdote.
- Content is right for the market at write-time, stale 45 days later.
- SEs and AEMs have tribal knowledge that's not written down anywhere. Jim: "Anmol knows it. It's going to take work to get it from his head to paper in a way I can train others from."

**Ideas surfacing in conversations:**
- Notebook LLM + Attention call transcripts as a real-time content intelligence engine. Gary is already doing this personally. Jim is interested.
- AI-driven win/loss synthesis from Salesforce/Slack/Attention data.
- "Agent-driven enablement" — the same way engineers are now supervisors of 50 agents, the PMM should be generating and updating content with AI.
- Slack channel for content drops (instead of drive folders nobody opens).

---

### Theme 8: Competitive & Market Context Is Changing

**The signal:** Gary: "After re:Invent wore off, it was anyone's game. Everybody agrees AI can solve this problem. Everybody. That's our challenge." Brandon: "Human X had to send an apology email for the spam. There is just too much noise going out."

**The competitive dynamics:**

**DataDog with AI:** The default objection. "DataDog does this." Gary's response: "Resolve minus DataDog is what you're paying for." The right counter is our cross-stack correlation, compounding knowledge, and context we have that single-tool vendors don't. We're not saying it clearly.

**Build vs. buy:** Coming up more frequently. Josh: "Everybody in developer-led orgs is already building internal agents. Skills. MCP. It's easy now." The answer isn't fear — it's alignment: "Great, what you've built with Skills is exactly why Resolve works better for your team. Here's how." Prodan floated a Trojan horse: a free skills linter tool that helps dev teams manage consistency of their agent config files — and seeds the data/context we need for Resolve.

**Claude Code / Cursor:** These are in the same conversation now. Prodan's product insight is compelling: there's a PRD for agent-to-agent protocol so Claude Code can call Resolve when a problem is too hard for it to solve locally. This could be a major partnership/distribution angle.

**Market shift from 2025 to 2026:** Josh: "If you go back to our evaluating an AI SRE blog, it doesn't mention what it's doing with other agents, what the future looks like, or the inputs and outputs. It no longer sounds right." The market has moved. AI readiness is now a board-level topic. Execs want usage metrics across all AI tools. The conversation isn't "will AI solve this?" — it's "how do we prove we're adopting AI at the right pace?"

---

## Action Plan

### Tier 1: Must Do Now (Next 2 Weeks)

**Action 1: Build the Discovery/First Call Deck (S0→S2)**
*Source: Bharath/Pawan, Gary/Pawan, Brandon/Pawan*
The deck should have 5–7 slides max: Who we are/why you should care → What we're hearing from the market → Two customer stories (Coinbase/Salesforce style with real outcomes) → Product demo → How we work with you → Vision slide. Bharath's framework is right. The discovery questions are the most important element — every slide should have a companion question to get the customer talking. Exit criteria: AE can fill out a discovery template after S1.

**Action 2: Document the Differentiator Story (Internal First)**
*Source: Gary/Pawan, Brandon/Pawan, Jim/Pawan*
One page. What makes Resolve different at three levels: (1) Company-level moat (team, full-stack AI ownership, research-led), (2) Platform-level moat (cross-stack correlation, compounding knowledge flywheel, always-on), (3) Deal-level proof (how long it took Salesforce, what Coinbase saw at month 6 vs. month 1). This doc feeds every other artifact: deck, SDR scripts, demo narrative, email sequences.

**Action 3: Codify the POC Playbook Based on What's Working**
*Source: Vasi/Pawan, Prodan/Pawan, Brandon/Pawan*
Take Vasi's pre-flight document and the Project Perseus framework and turn them into the standard. One POC track. Success criteria don't change deal to deal. The pre-flight doc is the S2 exit gate — you don't start POC without it. Include: named POC DRI, prioritized alert buckets, tool access list, timeline, roles (user/reviewer/deployer/security owner), and the "wheel of happiness" expectation-setting script.

**Action 4: Create 2–3 Flagship Customer Stories**
*Source: Multiple transcripts*
Each story should be structured as: who the customer is (engineering context) → what the pain was → what was required to set up → what happened by day 30/60/90 → outcome in their language. Candidates: Coinbase (production, 2x usage), Salesforce (incident response), Millennium (auto-investigations unlock). These stories go in the first call deck, SDR outreach, and website.

---

### Tier 2: Do This Month (April)

**Action 5: Define and Document ICP — Both Archetypes**
*Source: Josh/Pawan, Prodan/Pawan, Gary/Pawan*
Document Archetype A (developer-led, embedded SRE) and Archetype B (centralized NOC/SRE) with: company profile, who we talk to first, who we need to reach eventually, common objections, POC setup requirements. This informs SDR targeting, qualification questions at S1, and which play we run in scoping.

**Action 6: Fix the "AI for Prod" Messaging for the Field**
*Source: Gary/Pawan, Victor/Pawan, Verbal Identity Regroup*
Two versions of the core message: (1) Vision-level for EBs — don't lead with MTTR, lead with AI readiness, engineering velocity, and the compounding value of a system that gets smarter. (2) Practitioner-level for application teams — "Imagine a new team member who knows your entire stack, your runbooks, and your tools, and is highly coachable." Test both in the next 3 weeks of calls.

**Action 7: Write the Build vs. Buy Playbook**
*Source: Multiple*
One-pager for sales + SE: when does this objection come up, what's the right response, what evidence do we have. The frame isn't "don't build it" — it's "what you've already built with Skills and Claude Code is why Resolve works faster for you. Here's the gap we fill."

**Action 8: Customer Usage Dashboard — Push for Product Priority**
*Source: Brooke/Pawan*
Customers need visibility into their own usage. We need it for expansion conversations. Align with product on timeline. In the interim, Brooke/Victor team should create a manual "customer success scorecard" that gets shared weekly with the senior sponsor.

---

### Tier 3: Next Quarter

**Action 9: Build the Golden Onboarding Path**
*Source: Victor/Pawan, Anmol/Pawan, Jim/Pawan*
A sequenced, gated onboarding experience: (1) Connect top 3 integrations, (2) Fill out team dictionary, (3) Create first Resolve MD file for one service, (4) Run first investigation, (5) Set up auto-investigation for 5 alerts. Each step with an expected outcome, a "check your work" prompt, and a timer. Target: customer is self-sufficient on the basics within 10 days of contract.

**Action 10: Agent-Driven Enablement System**
*Source: Jim/Pawan, Gary/Pawan*
Build the PMM Copilot flywheel: Attention transcripts + Salesforce win/loss data → automated weekly synthesis → updated messaging brief → Notebook LLM audio overview for the field → 15-minute Slack update. Jim is ready to partner on this. Gary is already doing parts of it manually.

**Action 11: Free Skills Linter / Trojan Horse Tool**
*Source: Prodan/Pawan, Swarit/Pawan*
Validate the concept with engineering: can we build an open-source tool that lints and manages consistency across a team's Skills packages? If yes, this is a developer-led pipeline play that seeds Resolve context and surfaces the right ICP inbound.

---

## Key Quotes to Anchor This Work

> "We don't have use cases that differentiate us against the market in any way." — Gary (SDR/Outbound Lead)

> "We get 90 meetings in and nobody's asked the customer what their engineering initiatives are this year. That's the only question that matters." — Bharath

> "I've never had this conversation with anyone on the team. This is just what I've been doing." — Vasi, describing his POC methodology

> "The real differentiator is long-term value with Resolve AI. You're not going to have to go month by month trying to find the best approach. It's like investing in Salesforce in 2007." — Gary

> "The minute they had a live incident and Resolve worked, the entire leadership was convinced. That has more value than any constrained POC." — Swarit

> "Our demos are indistinguishable from every other demo in the market. Here's a giant chat list of text and context you've never seen before. It doesn't tell you anything you didn't know from the website." — Brandon

> "Imagine you hired a new person on your team who knows your whole stack, your runbooks, every tool you use, and is highly coachable. That's Resolve." — Victor

> "Over-communication is the mother of learning. You need to send them the plan every week. They should be able to memorize the dates in their sleep." — Vasi

---

## What We Still Need to Learn

The following topics came up but weren't fully explored — and should be prioritized in follow-up conversations:

- **Competitive deals:** Who else is showing up in active evaluations? What's their demo look like? (Talk to: AEs with active competitive deals, Manveer)
- **Win analysis:** What specifically happened in our 5 most recent wins at S3+? (Talk to: Anmol, specific AEs)
- **Loss analysis:** What happened in the 5 most recent POC losses? (Access: Salesforce, Attention calls on closed-lost deals)
- **Dave / Daniel:** These conversations weren't captured with sufficient transcript detail — follow up on what they're seeing from their vantage points.
- **New AEs onboarding experience:** What are Jordan and others running into in their first 60 days? What do they still not understand about the product?

---

*Document generated from 14 Granola meeting transcripts, March 23–April 7, 2026*
*Next update: April 21, 2026*
