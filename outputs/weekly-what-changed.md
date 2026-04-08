# What Changed This Week
Date: 2026-04-08
Period: Current snapshot (Dec 2025 – Apr 7, 2026)
Audience: Sales reps (AE / SDR / SE)
Sources reviewed:
- `outputs/granola-listening-tour-analysis.md` (**NEW** — 14 cross-functional sessions, Mar 23–Apr 7, 2026)
- `outputs/voice-of-customer-q1-2026.md` (25 first calls/demos, Dec 2025–Mar 2026)
- `outputs/attention-calls-pmm-analysis-s1-s4.md` (25+ calls, Feb–Apr 2026, S1–S4 deal stages)
- `docs/calls/ticketmaster-first-call.md` (S1 discovery, Apr 2026)
- `outputs/resolve-positioning-document.md` (positioning, April 7, 2026)
- `docs/competitors/competition.md` (competitive positioning)

---

## Customer Signal Shifts

### New or stronger pains

- **Alert fatigue is the door-opener** — 18 of 25 first calls raised it. Ticketmaster's Principal SRE led their entire discovery with it — not MTTR, not investigation time. Teams receive so many alerts that engineers stop looking at anything below P1. _"If they properly analyze all of alerts, it will be a full day job to simply answer alerts. At some moment, teams who got too many alerts, simply ignore alerts."_ — Yevhen Zavhorodnii, Principal SRE, Ticketmaster. Source: `ticketmaster-first-call.md`, `voice-of-customer-q1-2026.md`

- **Hero culture and tribal knowledge at organizational scale** — Named explicitly by Ticketmaster and echoed in 22 of 25 VoC calls. A small group of senior engineers know how everything works. When they're not on call, incidents take twice as long. When they leave, the knowledge walks out the door. _"I would prefer not using human beings as knowledge base."_ — Yevhen Zavhorodnii, Ticketmaster. _"Tribal knowledge. So we have an engineer that quits and then, you know, that knowledge is out the door. It's not documented anywhere."_ — SRE Lead, Veeva. Source: `ticketmaster-first-call.md`, `voice-of-customer-q1-2026.md`

- **"We know what happened — not why"** — The clearest buyer articulation of the core pain. Worth mirroring directly in discovery. _"We know what's happening, what is broken, but we do not know why and how to go about it. That's where we spend the majority of time."_ — TIAA Operations leader. Source: `attention-calls-pmm-analysis-s1-s4.md`

- **The cold start problem** — On-call engineers who inherit an active P1 and have no context to begin. Multiple simultaneous symptoms, no clear starting point, slow escalation. _"When you're jumping into on-call and you have no idea where to start. You just see that something is on fire and you don't even know what is on fire."_ — Yevhen Zavhorodnii, Ticketmaster. Source: `ticketmaster-first-call.md`

- **"AI readiness" is now a board-level question for engineering leaders** — NEW from listening tour. The conversation has shifted from "can AI solve this?" to "how do we prove we're adopting AI at the right pace?" Executives want usage metrics across all AI tools. This creates an opening with VPs and CTOs who have an AI mandate and budget. _"Execs want usage metrics across all AI tools."_ Source: `granola-listening-tour-analysis.md`

### Desired outcomes gaining importance

- **"Show value in a week"** — Buyers in evaluations are setting their own time-to-value expectations — and they're confident Resolve can hit a one-week bar. _"If this is your bread and butter, that's what it is. Just implement it. You should be able to show value in a week."_ — Jay Rudrachar, Observability Lead, TIAA. Source: `attention-calls-pmm-analysis-s1-s4.md`

- **Live incident validation over POC results** — NEW from listening tour. When a real incident happens during evaluation and Resolve resolves it, leadership is convinced faster than any structured POC result. _"The minute they had a live incident and Resolve worked, the entire leadership was convinced. That has more value than any constrained POC."_ — Swarit, Resolve. Ask in S2: "If a P1 happened tomorrow and Resolve caught it — who on your team would need to see that?" Source: `granola-listening-tour-analysis.md`

- **Auto-generated, cited postmortems** — A standout demo moment for technically sophisticated buyers. Not just root cause — a fully cited, hyperlinked report the whole team can inspect and audit. _"It has a very cited postmortem where it's like, multiple of us have looked at it and we're like, geez, it has a lot of citations, it has a lot of links to all the stuff."_ — Brandon Zimmerman, Senior SRE, Block/Square. Surface this when auditability or post-incident review is named as a pain. Source: `attention-calls-pmm-analysis-s1-s4.md`

- **No new tool to learn** — Buyers don't want to replace their stack — they want intelligence across it. TIAA explicitly attributed their continued evaluation to this. _"Resolve really helps because it doesn't have a single source of truth. It operates within the tools that you have and the environment that you have."_ — TIAA. Source: `attention-calls-pmm-analysis-s1-s4.md`

---

## Competitive Changes

- **Datadog AI / Splunk AI** — The default objection in almost every deal. _"How is this different from Datadog with AI mode turned on?"_ The answer that's landing: cross-stack correlation. Single-vendor AI only sees one data silo. When an incident spans Splunk logs, Kubernetes state, and a recent deployment, no one tool's AI can investigate across all three. Resolve does. Trap question that opens the conversation: _"When your last major incident touched more than one tool — say Datadog and Kubernetes and GitHub — which of those investigated across all three simultaneously?"_ Source: `granola-listening-tour-analysis.md`, `competition.md`

- **Internal build / DIY agents (Claude + MCP, internal AI teams)** — Coming up more frequently, especially at developer-led orgs. The angle that's working: make it additive, not adversarial. _"What you've already built with Skills and Claude Code is exactly why Resolve works better for your team. Here's the gap we fill: cross-team incidents, persistent organizational knowledge, governance at scale."_ For the numbers: building what Resolve does typically requires 10–15 engineers, $10M+, and 18–24 months — and starts degrading when team members change. DoorDash evaluated this path and walked away. Source: `granola-listening-tour-analysis.md`, `competition.md`, `attention-calls-pmm-analysis-s1-s4.md`

- **Claude Code / Cursor** — NEW signal from listening tour. These are now in the same conversation as Resolve in some accounts. The distinction that matters: coding agents handle deterministic tasks in local context; Resolve handles non-deterministic production troubleshooting with live cross-stack signals. They're complementary, not competitive. There's a product roadmap angle here (agent-to-agent protocol: Claude Code calls Resolve when a problem is too hard for it to solve locally) that's worth raising in exec conversations. Source: `granola-listening-tour-analysis.md`

- **ServiceNow (FSI-specific)** — Hard procurement gate at TIAA. Not a preference — a compliance requirement. _"ServiceNow integration is a must have."_ Add to FSI discovery qualification: "Is vendor approval tied to ServiceNow marketplace listing?" Source: `attention-calls-pmm-analysis-s1-s4.md`

---

## What to Emphasize This Week

### 1. Try the "new team member" framing with practitioners

- **Stronger angle in market:** When talking to on-call engineers or SRE leads, try framing Resolve as a new person, not an AI platform. Victor (post-sales SE) uses it and buyers immediately know how to engage. _"Imagine you hired a new person on your team who knows your entire stack, your runbooks, and every tool you use — and is highly coachable. That's Resolve."_
- **Why it matters:** Practitioners know how to work with a knowledgeable colleague. They don't always know what to do with "AI for production." The person framing reduces skepticism and opens a natural conversation about what they'd want that person to know.
- **Proof:** Victor: _"When I say 'imagine you hired a new team member,' people immediately get it. They know how to interact with a person."_
- Source: `granola-listening-tour-analysis.md`

### 2. Open with the "engineering initiatives" question before any product talk

- **Add to discovery:** Before you get to MTTR or incidents, try: _"What are the top 2–3 engineering initiatives your team is running this year — and where does production reliability show up in that list?"_
- **Why it matters:** Buyers who connect Resolve to an active initiative (AI mandate, reliability OKR, headcount freeze) have a forcing function to move forward. Buyers who don't see that connection stall between S1 and S3.
- **Proof:** Bharath (Resolve internal): _"We get 90 meetings in and nobody's asked the customer what their engineering initiatives are this year. That's the only question that matters."_
- Source: `granola-listening-tour-analysis.md`

### 3. Lead with alert fatigue before MTTR stats

- **Lead with:** _"How many alerts does your team actually investigate each day — and what happens to the rest?"_ Let the buyer describe learned helplessness before you introduce any numbers.
- **Why it matters:** Buyers who lead with alert volume are already telling you they've given up on full coverage. Resolve's "100% of alerts investigated" stat (Zscaler) lands as relief, not a claim to scrutinize.
- **Proof:** _"In a week, they're not gonna look at every single alert."_ — SRE Lead, Alation. Zscaler: 100% of 150,000+ monthly alerts now investigated.
- Source: `ticketmaster-first-call.md`, `voice-of-customer-q1-2026.md`

### 4. Use the compounding knowledge story for CTO/VP conversations

- **Lead with:** _"Every investigation Resolve runs makes the next one more accurate — and that organizational knowledge compounds. At month six, Coinbase's engineers said writing code was no longer the bottleneck. The investigation layer was getting smarter on its own."_
- **Why it matters:** Executive buyers at AI-forward companies want to understand what they're investing in over time, not just the first 30 days. The flywheel story (Salesforce in 2007 framing) resonates with long-term thinkers and makes the deal feel strategic, not tactical.
- **Proof:** Gary (SDR Lead): _"It's like you're investing in Salesforce in 2007."_ Coinbase: 250+ weekly investigation sessions at month 6 — Resolve became the default investigation surface.
- Source: `granola-listening-tour-analysis.md`, `outputs/resolve-positioning-document.md`

### 5. Anchor "customers as canaries" for the business risk conversation

- **Add to discovery:** When buyers describe customer-reported incidents, try: _"So your customers know about the problem before your monitoring fires — what does that mean for your business when it happens?"_ Let them name the consequence.
- **Why it matters:** MTTR is a metric. Being surprised by a customer tweet before your own alerts fire is a story. It surfaces board-level and revenue impact without you stating it.
- **Proof:** _"Customers act as canaries so they find the problem before we do."_ — Anestis Samaras, Group Head of Data Science, LBG.
- Source: `attention-calls-pmm-analysis-s1-s4.md`

---

## Rep-Ready Actions This Week

1. **Discovery question:** _"When your team gets paged at night, how long before your customers know there's an issue — and how long before you know?"_ Surfaces detection lag and makes the buyer name the business risk themselves. Works with SRE leads and engineering executives alike.

2. **Build vs. buy response:** _"What you've already built with Skills and Claude Code is exactly why Resolve moves faster in your environment — it uses what you've invested in. The gap we fill is everything that breaks when incidents cross team boundaries: persistent knowledge, cross-stack correlation, governance at scale. Building that yourself typically lands at 10–15 engineers, $10M+, 18 to 24 months. DoorDash ran that analysis and chose Resolve."_

3. **Competitive qualification question:** _"When your last major incident touched more than one tool — say Datadog metrics and Kubernetes state and a recent deployment — which of your current tools investigated across all three simultaneously?"_ Buyer answers the question for you.

4. **Proof point to lead with (SRE persona):** _"At DoorDash, Resolve found root cause in 15 minutes. Their engineer took a different path — came back 105 minutes later, and Resolve's original finding was correct. On a $1B+ ads platform, that 90-minute gap represents up to $200K per incident in potential revenue exposure."_ Specific, narrative, revenue-anchored. Avoids the abstract-percentage skepticism ("sounds too good to be true").

5. **On calls, prefer saying ___ over ___:**
   - Say **"works across the tools you already have"** over "platform" — "platform" implies replacing your stack; buyers flinch at that word
   - Say **"AI incident response automation"** over **"AI SRE"** — "AI SRE" creates category confusion; use "AI incident response" in first calls, "production intelligence" in exec conversations
   - Say **"investigation"** over **"AIOps"** — buyers map AIOps to alert correlation tools (Moogsoft, PagerDuty); Resolve investigates, not just correlates

---

## Proof Points & Language to Use

**Strongest customer-backed lines this week:**

- _"Imagine you hired a new person on your team who knows your entire stack, your runbooks, and every tool you use — and is highly coachable. That's Resolve."_ — Victor, post-sales SE (field-tested framing that closes faster with practitioners)
- _"Customers act as canaries so they find the problem before we do."_ — LBG Group Head of Data Science (opens the detection-lag conversation)
- _"We know what's happening, what is broken, but we do not know why and how to go about it. That's where we spend the majority of time."_ — TIAA (mirror this in discovery)
- _"The minute they had a live incident and Resolve worked, the entire leadership was convinced."_ — Swarit, Resolve (use to set up the POC framing)
- _"I would prefer not using human beings as knowledge base."_ — Ticketmaster Principal SRE (hero culture conversation)
- _"Our SRE team is not going to double in size and we're not gonna be able to afford to."_ — ADT Head of Software Engineering (headcount leverage for VPs)
- _"You should be able to show value in a week."_ — TIAA (let the buyer set the POV bar)
- _"It's like investing in Salesforce in 2007."_ — Gary, Resolve SDR Lead (compounding value for exec conversations)

**Stats that land in the field:**
- DoorDash Ads: **87% faster** root cause. Investigation time from 40 minutes to under 5.
- Coinbase: **72% faster**. 250+ weekly investigations across 100+ engineers at month 6.
- Zscaler: **30% fewer engineers per incident**. **100%** of 150,000+ monthly alerts investigated.
- Fortune 50: **60–80% MTTR reduction** across 160,000 investigation hours/year.

**Terms that create friction on calls:**
- "AI SRE" — creates confusion about category; buyers don't yet have a clear mental model
- "AIOps" — maps to alert correlation in buyers' minds (Moogsoft, PagerDuty), not root cause investigation
- "Platform" used alone — implies stack consolidation; use "works across your existing stack" instead
- Abstract percentages without a story — _"sounds too good to be true"_ (BlackRock) — lead with the narrative, follow with the number

---

## NotebookLM Asset Prompts

**Audio briefing prompt:**
"Generate an upbeat, practical 5-minute Monday morning audio briefing for an AE heading into first calls this week with enterprise SRE and engineering leaders. Make the rep the hero — they're walking in prepared and confident. Cover: (1) the two strongest opening questions to get a buyer talking about real pain in the first 5 minutes, (2) the framing that's landing fastest with practitioners right now ('new team member' angle), (3) how to handle the Datadog AI objection in one crisp paragraph, and (4) the one proof point that's working best with SRE personas. Keep it conversational — no bullet lists."

**Quiz prompt:**
"Quiz me on competitive scenarios. I'll give a response and you score whether it would advance a deal. Scenarios: (1) Buyer says 'We have Datadog and they have AI features now — what do you do differently?' (2) Buyer says 'Our team is already building with Claude and MCP, why would we buy Resolve?' (3) Buyer says 'Your 87% improvement number sounds too good to be true for our environment.' For each answer I give, tell me: what landed, what fell flat, and give me the sharper version from a rep who's won this deal before."

**Role-play prompt:**
"Play the role of a skeptical VP of Engineering at a 1,500-engineer fintech. You have Datadog and Splunk deployed. Your team already experimented with an internal Claude-based agent. You have an AI mandate from the board but you've been burned by tools that over-promised. You'll push back on vague answers and ask for specifics. Raise these in order: (1) 'We tried building something similar last year — why is Resolve different?' (2) 'Walk me through exactly what would happen in our environment on day one.' (3) 'Our CTO is going to ask me what the ROI is — what do I tell him?' Stay skeptical but open. Stop and give feedback if you hear a response that would actually make you want to schedule a demo."
