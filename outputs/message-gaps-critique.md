# Message Gaps Critique
Date: 2026-04-07
Positioning docs reviewed: `docs/positioning/EXAMPLE-current-positioning-v3.md` (Resolve AI positioning doc, April 7 2026)
Research docs reviewed: `outputs/research-synthesis.md`, `outputs/attention-calls-pmm-analysis-s1-s4.md`, `docs/calls/ticketmaster-first-call.md`, `docs/competitors/competition.md`

---

## Pre-Scoring: List A vs. List B

### List A — What WE Say
*(All distinct claims, phrases, and positions in current positioning doc)*

**Taglines / category claims:**
- "AI for prod platform"
- "closes the loop from alert to root cause — automatically, across every tool in the stack"
- "Production intelligence platform"
- "AI incident response automation"
- "Most of the time your engineering team loses isn't from fixing issues — it's from figuring out what's going on"

**Capability labels used internally:**
- "Post-Trained Models on Real Production Patterns"
- "Organizational Intelligence Layer — The Multiplayer Moat"
- "Evidence-Backed Causal Chain"
- "Satellite Architecture — Security-First Design"
- "multi-agent: planner + sub-agents + critique agent"
- "Altitude 1 / Altitude 2" messaging

**Customer language used:**
- "war room," "bridge call," "paged at 2am," "tribal knowledge," "on-call toil"
- "30-engineer war room shrinks"
- "3 people who know the system"
- "production is where the velocity goes to die"

**ICP definition:**
- Primary: "Service Owners at Engineering-Led Companies" — engineering managers, senior engineers who write the code and own on-call for their service
- "The right entry persona is NOT SRE or platform engineering"

**Proof points used:**
- DoorDash 87% faster, Coinbase 72%, Zscaler 75%/30%, Fortune 50 60-80%
- DoorDash walked away from the build path

---

### List B — What THEY Say
*(Recurring themes, priorities, and language from customer research — verbatim or close to it)*

**Visceral pain language:**
- "Customers act as canaries so they find the problem before we do" — LBG
- "20+ engineers on a single bridge" — LBG, HSBC
- "Zoo of systems" — Ticketmaster framing
- "We know what's happening, what is broken, but we do not know why" — TIAA
- "Not getting a result in 30 minutes is like holy crap" — Block/Square
- "Fully analyzing alerts would take an entire workday" — Ticketmaster
- "Hero culture / constant firefighting" — Ticketmaster
- "Cold start" — on-call engineers who don't know where to begin
- "Our SRE team is not going to double in size" — ADT
- "Our teams are constantly being asked to do more with less" — McKinsey
- "Fragmented knowledge that usually lies in meetings, in messaging, but also in runbooks" — HSBC

**What success looks like (customer words):**
- "Root cause found correctly. Nice." — Adobe
- "Show value in a week" — TIAA
- "It's replacing also the unnecessary human reviewer" — LBG conversation
- "It doesn't have a single source of truth. It operates within the tools that you have" — TIAA

**Questions/objections that define the buyer journey:**
- "What do you do that we wouldn't be able to do ourselves?" — HSBC (every S1/S2)
- "How is this different from what coding agents already do?" — ADT
- "Are you proactively looking at logs?" — LBG (proactive vs. reactive)
- "That is only 30% of our change." — TIAA (change detection scope)

---

## Overall Verdict
**Score: 16/25** — The positioning foundation is strong and above average for this category. The core thesis ("time lost is in figuring out, not fixing") is differentiated and true. Proof points are real and compelling. However, the messaging operates at a conceptual altitude that misses the most visceral customer language: the bridge call with 20+ engineers, the hero culture burning out the team, and the canary problem where customers find your failures first. The ICP definition is the single most consequential gap — calling SRE/platform teams the "wrong first call" contradicts every deal pattern in the research. The capability names (Post-Trained Models, Organizational Intelligence Layer, Satellite Architecture) are internal framing that customers never use and that translate features, not outcomes, to buyers.

---

## Dimension Scores

| Dimension | Score | Top Issue |
|-----------|-------|-----------|
| Language Match | 3/5 | Missing the most visceral customer phrases; capability sections use internal jargon customers never say |
| Pain Coverage | 3/5 | Hero culture, cold start problem, and alert fatigue as an *entry point* are absent despite appearing in every account |
| Outcome Clarity | 3/5 | Attribute sections (Post-Trained Models, Satellite Architecture) describe features, not buyer outcomes |
| Competitive Differentiation | 4/5 | "Multiplayer" org intelligence and post-trained models are genuinely unique; headline language is partially table stakes |
| Evidence Credibility | 3/5 | Strong outcome metrics; weak organizational knowledge narrative; ICP definition contradicted by call data |

---

## Detailed Findings

---

### Dimension 1: Language Match — 3/5

**Terms WE use that customers never say (retire or translate):**
- "Post-Trained Models on Real Production Patterns" — no customer has ever asked for this. Translate to outcome: "AI that's been trained on real production failures, not textbooks."
- "Organizational Intelligence Layer" — internal architecture framing. Customer version: "the institutional memory that doesn't leave when your best SRE does."
- "Multiplayer" / "single-player" — clever analogy, but no customer uses these words. Consider "team-level" vs. "one engineer at a time."
- "Satellite Architecture" — security teams understand this; engineering buyers don't lead with it.
- "Multi-agent: planner + sub-agents + critique agent" — spec language. Customers care what it produces, not how it's wired.
- "Altitude 1 / Altitude 2" — internal presentation framing, not customer language.
- "Engineering-led companies" — qualifier that customers never use to describe themselves.
- "Causal chain" — adjacent to customer language but not how they describe it; they say "root cause" or "why it happened."

**Terms customers use frequently that we underuse or ignore:**

| Customer phrase | Source | Why it belongs in messaging |
|---|---|---|
| "Customers act as canaries" | LBG (multiple contacts) | Most emotionally loaded description of the detection gap — customers finding failures before you do is a boardroom shame event, not just an MTTR number |
| "20+ engineers on a single bridge" | LBG, HSBC | Visceral and specific. "30-engineer war room" is close but less precise |
| "Zoo of systems" | Ticketmaster framing | Instantly recognizable to any SRE at a large company. Better than "fragmented tooling" |
| "Hero culture" | Ticketmaster | Names the organizational dysfunction behind on-call burnout — resonates with engineering leaders |
| "Cold start" | Ticketmaster | Specific SRE term for the "new on-call engineer doesn't know where to begin" problem |
| "We know what happened, not why" | TIAA | The exact buyer pain in 7 words — cleaner than any internal framing |
| "The whole thing should resolve in 15–20 minutes" | Block/Square | Sets the time expectation buyers have; makes 40+ minutes feel unacceptable |
| "Not my team" | Implied across HSBC/LBG | The bridge call moment where an engineer is cleared — the outcome buyers want |
| "Know before your CEO does" | Referenced in prior notes | Boardroom pain in 5 words |

---

### Dimension 2: Pain Coverage — 3/5

**Top 5 pains ranked by frequency — coverage assessment:**

| Pain | Customer Frequency | In Our Messaging? |
|---|---|---|
| High MTTR / customers find issues first | 6+ sources | INDIRECT — framed as "time lost figuring out what's going on," but the "canaries" shame moment is absent |
| Fragmented tooling / no end-to-end picture | 5+ sources | WELL COVERED — "across every tool in the stack," competitive framing vs. single-vendor AI |
| Alert fatigue / engineers only respond to critical | 3+ sources | ABSENT as an entry point — only surfaces in competitive comparison context |
| Overcrowded bridge calls | 4+ sources | PARTIALLY COVERED — "war room," "30-engineer war room shrinks" mentioned but not led with |
| Knowledge locked in senior engineers | 4+ sources | WELL COVERED — "institutional memory," "3 people who know the system," "tribal knowledge" |

**Biggest uncovered pain:** Alert fatigue as a *primary entry point*. Ticketmaster's Principal SRE opened the call with this — "fully analyzing alerts would take an entire workday." This is a door-opener with on-call engineers that the positioning never surfaces. The current messaging assumes buyers are already motivated to improve RCA; alert fatigue is what makes them look for a solution in the first place.

**Other notable gaps:**
- **Hero culture / unsustainable on-call burden** — Ticketmaster named this explicitly. It's the human, organizational version of the MTTR problem. Nowhere in the positioning doc.
- **Cold start problem** — on-call engineers who inherit incidents they don't understand. Directly addressable by Resolve's organizational knowledge layer, but never connected to this pain.
- **"Customers as canaries"** — the moment of board-level embarrassment when a customer tweets about your outage before your own monitoring fires. This is the buying trigger, not just a pain. Not in the messaging.

---

### Dimension 3: Outcome Clarity — 3/5

**Where we describe outcomes well:**
- "Engineers start incidents with answers instead of questions" ✓
- "The 30-engineer war room shrinks because anyone — not just the person who 'owns' that service — can start with full context" ✓
- Customer value section (Section 3) with %% improvement metrics ✓
- "Production knowledge accessible in seconds, not locked in three people's heads" ✓

**Where features are described instead of outcomes (with suggested fixes):**

| Feature framing we use | Outcome translation |
|---|---|
| "Post-Trained Models on Real Production Patterns" | "AI that's learned from thousands of real production failures — not labs or demos — so it knows which signals matter and which don't" |
| "Multi-agent: planner + sub-agents + critique agent in parallel" | "Resolve runs investigations the way a senior SRE would — checking multiple hypotheses at once, not one log at a time" |
| "Evidence-Backed Causal Chain, Not Black Box Output" | "Every conclusion comes with the receipts — which logs, which queries, why this hypothesis over that one. Engineers interrogate it like a colleague, not trust it like a black box" |
| "Satellite Architecture — Security-First Design" | "Your data never leaves your environment — Resolve queries your tools in place. The security review that took 6 months at [competitor] takes days with us" (needs specific proof point) |
| "Organizational Intelligence Layer" | "The institutional memory that doesn't leave when your best SRE does" |

The Section 2 (Unique Attributes) structure is internally logical but reads like a product spec to a buyer who just wants to know: will this stop the 2am calls? Every attribute section should open with the buyer's lived moment, not the capability label.

---

### Dimension 4: Competitive Differentiation — 4/5

This is the strongest dimension. Resolve has genuinely differentiable claims.

**Genuinely unique (competitors cannot say the same):**
- "Multiplayer" organizational intelligence — cross-engineer, cross-team knowledge that persists: **NO direct competitor makes this claim with evidence**
- Post-trained on real production patterns at named enterprises (DoorDash, Coinbase, Zscaler): **NO competitor has comparable training data story**
- Founded by OpenTelemetry creators: **credibility anchor that's unrepeatable**
- $150M raised, production since 2024 vs. AI SRE startups launching 2025: **category timing and capital advantage**
- DoorDash "walked away from the build path" — a named customer validating build vs. buy: **powerful and specific**

**Table stakes / could be said by any competitor:** [TABLE STAKES]

| Our claim | Why it's undifferentiated |
|---|---|
| "Closes the loop from alert to root cause" | [TABLE STAKES] Every AIOps vendor uses "root cause" language |
| "Works across existing tools without replacing them" | [TABLE STAKES] Every observability vendor claims integration breadth |
| "AI incident response automation" | [TABLE STAKES] Category label; doesn't differentiate within category |
| "Days to first investigation" | [TABLE STAKES] Competitors claim fast time-to-value too |
| "SOC 2 Type II, HIPAA, PCI-DSS" | [TABLE STAKES] Expected at enterprise; not a differentiator |
| "Enterprise-grade reliability" | [TABLE STAKES] Category language |

**Most dangerous gap:** The "build vs. buy" response in the positioning is still narrative-level. Competition doc has the hard numbers (10–15 engineers, $10M+, 18–24 months) but they don't appear in the main positioning document. Every S1/S2 call surfaces this question. The answer needs to be a crisp sentence with numbers, not a paragraph.

---

### Dimension 5: Evidence Credibility — 3/5

**Claims with strong customer evidence:** ✓
- 87% faster — DoorDash (with narrative) ✓
- 72% faster — Coinbase (with narrative + public quote from re:Invent) ✓
- 75%/30% — Zscaler ✓
- 60-80% MTTR — Fortune 50 ✓
- Build vs. buy — DoorDash walked away ✓

**Claims with NO or insufficient customer evidence:** [NO CUSTOMER EVIDENCE]

| Claim | Evidence status |
|---|---|
| "Every time a key engineer leaves, their production IP persists in Resolve" | [NO CUSTOMER EVIDENCE] — powerful claim, no customer story attached |
| "Engineers engage with Resolve the way they engage with a senior teammate" | [NO CUSTOMER EVIDENCE] — the Adobe SRE quote ("root cause found correctly, nice") is close but not used |
| "AI coding tools are accelerating code output... Resolve is the production layer" | [NO CUSTOMER EVIDENCE] — strong thesis, but no customer says this yet |
| "Every engineer and every agent as effective as your best SRE" | [NO CUSTOMER EVIDENCE] — aspirational vision claim with no proof |
| "Production is where the velocity goes to die" | [NO CUSTOMER EVIDENCE] — compelling framing, no customer validates it |
| "A global hedge fund eliminated its dedicated NOC role" | [NO CUSTOMER EVIDENCE NAMED] — powerful but anonymous; less credible than named customer stories |

**ICP definition — contradicted by research:** [CRITICAL]
The positioning doc states: "The right entry persona is NOT SRE or platform engineering." But across 25+ calls and the Ticketmaster transcript, the actual buyers are:
- Principal SRE (Ticketmaster)
- Head of SRE (multiple)
- Staff SRE Engineer (Block/Square)
- Group Head of Data Science (LBG)
- VP Platform Engineering

The "service owner / application owner" ICP is an internally-derived hypothesis. Call data does not validate it. This is the most dangerous evidence gap in the document — a go-to-market strategy built on an unchecked assumption.

---

## Priority Action List
*(Ranked by impact on message-market fit)*

### 1. Fix the ICP definition — it's contradicted by call data
**Action:** Remove the "service owner NOT SRE" primary ICP claim. Replace with a two-layer ICP grounded in calls: Champion = Head of SRE / Principal SRE / VP Platform Engineering (they drive POCs, they feel the pain, they are in every deal); Economic buyer = CTO / Group Head of Data Science / Head of Software Engineering (they sign, they champion AI internally, they care about headcount leverage).
**Expected improvement:** Reduces sales motion confusion, ensures outbound and AE talk tracks target the people who actually pick up the phone and drive evaluations.
**Evidence:** Every named buyer in 25+ calls is an SRE or platform eng leader, not a service owner. The "service owner" framing appeared in zero call transcripts.

### 2. Lead with "customers as canaries" — not "figuring out what's going on"
**Action:** Add the "customers as canaries" framing to the primary pain narrative. Before the thesis line ("most time lost is in figuring out"), establish why that matters: "By the time you figure out what happened, your customers already knew. They found it first." This converts an abstract efficiency message into a board-level shame and risk story.
**Expected improvement:** Increases emotional resonance at the first call; converts a "nice to have" evaluation to an "urgent problem" frame.
**Evidence:** Used by LBG (multiple contacts) and HSBC CTO — two of the most advanced deals in the pipeline. This is the moment in every S1 that makes prospects lean forward.

### 3. Add "hero culture" and "cold start" as named pain arcs
**Action:** Insert a named section or named pain frame covering: (a) unsustainable hero culture — one or two engineers who know everything and get paged every time; (b) the cold start — the new on-call engineer who inherits a P1 and has no context to start from. Both have direct Resolve answers (organizational knowledge layer) but those answers are currently orphaned from the pain they solve.
**Expected improvement:** Opens a second narrative arc beyond MTTR — the human and organizational dysfunction story that resonates with engineering leaders who don't see themselves as having an "MTTR problem" but do see themselves as having a "we rely on two people for everything" problem.
**Evidence:** Ticketmaster opened the discovery call with hero culture and cold start as primary pains. ADT, HSBC echoed it.

### 4. Weaponize "build vs. buy" with specific numbers
**Action:** Add a crisp, one-paragraph "build vs. buy" answer to the main positioning doc (not just the competitive appendix) with the hard numbers from the competition doc: 10–15 engineers, $10M+, 18–24 months to build a comparable system — and it starts degrading immediately when team members leave. The DoorDash narrative is powerful but needs the numbers alongside it.
**Expected improvement:** Converts the #1 S1→S2 stall point from a conversation-stopper into a proof point. Reps currently give a hand-wavy conceptual answer; a specific number gives them something to anchor on.
**Evidence:** Raised on every S1/S2 call at HSBC, ADT, McKinsey. Current answers described as "high-level and not crisp" in the call analysis.

### 5. Rewrite Section 2 (Unique Attributes) openings — features first, outcomes nowhere
**Action:** Each of the four attribute sections (Post-Trained Models, Org Intelligence, Evidence-Backed Causal Chain, Satellite Architecture) currently leads with a capability label. Rewrite each to open with the buyer's lived moment or pain, then explain the capability as the answer. See Dimension 3 table for suggested translations.
**Expected improvement:** Makes the positioning readable and resonant for an engineering leader doing research, not just a PMM reviewing an internal doc. The capability labels can stay as sub-headers — they just can't be the first thing a buyer reads.
**Evidence:** DoorDash SRE quote on the postmortem: "Root cause found correctly. Nice." — the value is in the output, not the architecture.

---

## Language to Steal Immediately
*(10 customer phrases that should appear verbatim or near-verbatim in messaging)*

| # | Phrase | Source | Why it's powerful |
|---|---|---|---|
| 1 | "Customers act as canaries so they find the problem before we do" | Anestis Samaras, Group Head of Data Science, LBG | Converts MTTR from a metric to a boardroom embarrassment story. Specific, visceral, memorable. |
| 2 | "20+ engineers on a single bridge" | LBG, HSBC | Specific number makes the waste concrete. "War room" is generic; "20+ engineers on a single bridge" is an image. |
| 3 | "We know what's happening, what is broken, but we do not know why" | TIAA Operations leader | The exact buyer pain in 14 words. Cleaner than any internal positioning sentence. Should be a pull quote in sales materials. |
| 4 | "Our SRE team is not going to double in size and we're not gonna be able to afford to" | Alexander Crettenand, Head of Software Engineering, ADT | The economic case for Resolve in one sentence. Better than any internal articulation of the "do more with less" value prop. |
| 5 | "Fully analyzing alerts would take an entire workday" | Yevhen Zavhorodnii, Principal SRE, Ticketmaster | Alert fatigue in concrete terms — not "we have noisy alerts" but a time cost. Opens the alert fatigue entry point. |
| 6 | "Hero culture / constant firefighting" | Ticketmaster discovery call | Names the organizational dysfunction that SRE leaders recognize instantly. Positions Resolve as the escape from hero culture, not just "faster MTTR." |
| 7 | "It's replacing also the unnecessary human reviewer" | Vasi Karkantzos, validated by LBG prospect | The "bridge call" outcome in specific terms — not "fewer engineers per incident" but the specific removal of the person who shows up only to say "not my team." |
| 8 | "It doesn't have a single source of truth. It operates within the tools that you have" | TIAA call (prospect's reaction) | The "no new system to learn" value prop in customer words. Directly addresses the top adoption objection. |
| 9 | "Root cause found correctly. Nice." | Adobe POC participant | The simplest possible articulation of Resolve doing its job. Can be used as a pull quote or in a social proof moment. Authenticity of the understatement is the point. |
| 10 | "You should be able to show value in a week" | Jay Rudrachar, TIAA | Customer setting the expectation for time-to-value — which Resolve can meet. Use to frame the POV process as matching what the buyer already expects. |
