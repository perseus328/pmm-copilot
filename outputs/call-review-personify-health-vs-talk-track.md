# Call Review: Personify Health (LP + Prodan) vs. S1 Talk Track

**Call**: Resolve AI x Personify Health — Discovery / Intro
**Reps**: Lauren "LP" Phillips (AE), Prodan Statev (SE), Brett (BDR)
**Prospect**: Ian Pina (Director DevOps/SRE), Elmedin Jasic (SRE Manager)
**Duration**: ~31 minutes
**Stage**: First call — sourced via re:Invent vendor list research

---

## OVERALL GRADE: B-

LP and Prodan run a decent discovery-first call. LP asks good questions in the first half, Prodan adds a smart "why" question, and they correctly pivot to demo when time is short. But several high-value talk track moments are missed, the tribal knowledge pain is sitting right there and nobody pulls the thread, and the call ends without a locked next step or multi-threading attempt.

---

## WHAT THEY DID WELL (Talk Track Aligned)

### 1. Discovery before demo — correct instinct
The talk track says: *"Don't jump to the demo before discovery. The best reps run 15+ minutes of step-by-step process questions before showing anything."*

LP does this. She spends the first ~16 minutes asking questions before showing anything. That's exactly right. She lets Ian and Elmedin talk, and she learns:
- 30% of SRE time spent on postmortem/RCA activities
- Stack: EKS, New Relic, PagerDuty, GitLab CI/CD, some Grafana/Prometheus
- Two-company merger (Virgin Pulse → Personify Health) with different maturity levels
- 250+ PagerDuty users across the org, but most don't know the incident process
- A real OKR: "20% productivity reductions by leveraging AI"
- VP of Platform Ops is the decision-maker; re:Invent meeting is the target

**Score: Strong.** This is what the talk track prescribes.

### 2. Tech stack discovery — asked early
The talk track says: *"What does your observability stack look like today?"*

LP asks this at 07:06: *"Could you maybe share a little bit more about like your tech stack and what the current flow looks like when an alert happens?"*

Ian gives a clean answer: EKS, New Relic (primary), some Grafana/Prometheus, PagerDuty, GitLab CI/CD, daily releases, AWS.

**Score: Good.** Got the basics.

### 3. Prodan's "why" question — excellent
The talk track doesn't explicitly script this, but the philosophy is right. At 15:27, Prodan asks:

> "Why is that a need? Like you said, we need to move fast, we need to improve things, we need to cut MTTR. Why?"

This surfaces the real driver: leadership pressure to show AI-driven productivity, a 20% productivity reduction OKR, and the fact that they haven't moved as fast as leadership wanted. That's gold — it tells you this deal has executive air cover and a measurable outcome they need to hit.

**Score: Excellent.** This is the kind of question that separates good from great.

### 4. LP's service ownership question — smart threading
At 08:20, LP asks about on-call expertise and siloization. This is a version of the talk track's tribal knowledge question. Elmedin's answer reveals:

> "A lot of the users out of those 250 plus don't really know what's going on exactly. Like they know their service, they know what they need to know, but when it comes to incident management and this side of the process, they're a bit lost."

**Score: Good question, but she doesn't pull the thread.** (See "What They Missed" below.)

---

## WHAT THEY MISSED (Talk Track Gaps)

### 1. THE TRIBAL KNOWLEDGE THREAD — left on the table

This is the biggest miss. The talk track says: *"When a senior engineer leaves your team — or gets reorged — what happens to that knowledge?"* and notes this is the #1 most emotionally resonant pain point across 2,000+ calls.

Elmedin literally hands them this pain on a platter:

> "We had a merger recently, trying to combine two different companies with different processes and different platforms into a single process... a lot of the users out of those 250 plus don't really know what's going on exactly."

And Ian adds:

> "The other half we call our TPA, which is basically... just a mess of ownership... just a lot of things that need to mature."

**Nobody asks**: "When those TPA engineers get paged at 3 AM for a service they didn't build, what happens? How long does it take them to even understand what they're looking at?"

That question would have surfaced the exact pain that makes Resolve's knowledge graph demo moment 10x more powerful. Instead, Prodan shows the knowledge graph at the end almost as an aside, and it doesn't land because the prospect hasn't emotionally connected to the problem it solves.

**Impact**: Missed the chance to make the knowledge graph the hero of the demo instead of a throwaway.

### 2. NO CUSTOMER STORIES WOVEN IN

The talk track peppers in Coinbase, Veeva, Ticketmaster, and Squarespace verbatims at specific moments. This call uses zero customer stories until LP vaguely mentions "a 73% reduction in MTTR for SEV zeros and sub ones" without naming the customer or telling the story.

**Where stories should have landed:**

- When Ian says "30% of engineering time on postmortem/RCA" → **Coinbase**: *"We had a similar situation at Coinbase — 160 K8s clusters, 200+ teams. Their SEV1/2 MTTR was 180 minutes. After rolling out Resolve, major incidents went from 2 hours to 20 minutes. 60% faster root cause detection."*

- When Elmedin describes 250 users who "don't really know what's going on" → **Ticketmaster**: *"Ticketmaster's SRE lead told us: 'I would prefer to not use humans as a knowledge base.' That's the problem Resolve's knowledge graph solves — it captures what your senior engineers know so everyone else can operate at their level."*

- When Ian mentions the TPA side being immature → **Coinbase adoption model**: *"At Coinbase, we started with one team in shadow mode. Teams started pulling Resolve in themselves — about 3 teams every 2 weeks. Now 206 engineers use it. The 'wellbeing first, then TPA' strategy actually maps perfectly to that pattern."*

**Impact**: The prospect left with "interesting technology" but no emotional proof that this works at companies like theirs.

### 3. THE "STEP BY STEP" PROCESS QUESTION — never asked

The talk track says: *"Walk me through what happens when a SEV1 fires. Step by step, from alert to resolution."*

LP asks about the tech stack and about who responds, but never asks the full workflow question. We learn fragmented pieces — PagerDuty alerts, 250 users, SRE team as primary responders — but we never hear the full incident lifecycle:

- How long from alert to first human eyes on it?
- How many tools do they open?
- How many people get pulled in?
- How long to root cause?
- What happens after — postmortem, action items, who writes them?

Ian volunteered "30% of time on postmortem/RCA" but nobody drilled into what that 30% actually looks like. Is it the investigation itself? The writing? The review meetings? That breakdown matters for scoping a POC.

**Impact**: They know the pain exists but don't have the specifics to build an ROI case or scope a demo properly.

### 4. NO USE CASE QUALIFICATION QUESTION

The talk track says: *"Of incidents, alert triage, and production debugging — which would move the needle most for your team right now?"*

This was never asked. They know Ian cares about MTTR and productivity, but they don't know which of Resolve's three use cases maps best to Personify Health. Is it incident investigation (the war room problem)? Alert triage (the noise problem with 250 PagerDuty users)? Or production debugging (the TPA knowledge gap)?

Prodan teases "vibe debugging" as the second use case but then doesn't show it — which is fine for time, but the prospect never got to self-select what matters most.

**Impact**: The demo they'll build for re:Invent will be a guess instead of tailored to what Ian's VP actually cares about.

### 5. NEXT STEPS — soft, not locked

The talk track says: *"Don't let 'let me run it by my manager' be the last thing said. Always lock a specific date."*

The call ends with:
- LP: "How about you and I get a one-on-one for early next week?"
- Ian: "Cool. Sounds great."

That's okay but soft. The talk track would have pushed for:
1. A specific day/time for the 1:1
2. The re:Invent meeting booked on calendar before hanging up
3. The "who else should be in the room" question

**Impact**: The follow-up depends entirely on email momentum, which is weaker than a calendar hold.

### 6. NO MULTI-THREADING ATTEMPT

The talk track says: *"Who else on your side should be in the room for the deep-dive?"* and warns about the SRE trap.

Right now the deal has two SRE-side contacts (Ian, Elmedin) and a VP they haven't met. Nobody asked:
- Are there app team leads on the wellbeing side who should see this?
- Who on TPA would benefit from understanding what's possible?
- Does your VP have a technical advisor who vets tools before he evaluates them?

**Impact**: This deal is at risk of the exact SRE trap pattern from the sales effectiveness analysis. Ian is enthusiastic but may not have the political capital to drive a purchase decision alone. The re:Invent meeting is a good sign, but it's a single-threaded path to the VP.

### 7. SATELLITE DEPLOYMENT — never mentioned

Ian works in healthcare (Personify Health). The talk track says to front-load satellite deployment for regulated industries. Nobody asked about data sensitivity, HIPAA, or where logs live. This will likely come up later as a blocker if not addressed proactively.

---

## DEMO SECTION: WHAT WORKED AND WHAT DIDN'T

### Worked:
- Prodan's walkthrough of the Slack-native experience is clean and practical
- Showing the investigation steps (logs → metrics → code → working theory) maps to the "evidence grounding" demo moment the talk track prescribes
- The knowledge graph / digital twin demo is a strong differentiator

### Didn't work:
- **No setup question before demo.** The talk track says: *"Is there a specific type of incident or alert pattern that would be most relevant for your team to see?"* Prodan showed a generic e-commerce feature flag incident. If he'd asked first, he could have picked something closer to Personify Health's world (healthcare services, EKS, New Relic-sourced alerts).

- **Evidence grounding not called out explicitly.** The talk track says to narrate: *"See how every claim has a citation?"* Prodan shows the work Resolve does but doesn't frame it as the "not a black box" differentiator. When Ian asks "is there data on how often the working theory is correct?" — that's the moment to say: *"That's exactly why we show every step. You can audit the reasoning, not just trust the answer."*

- **The accuracy question was handled okay but not great.** Ian asks about accuracy at 26:14. Prodan gives an honest answer (70% at DoorDash, lower initially, anchoring on helpfulness). That's fair. But the talk track would frame it differently: lead with the 60% faster RCA at Coinbase as the outcome metric, then explain that even when Resolve doesn't nail root cause, it eliminates the first 30 minutes of manual evidence gathering — which is exactly the 30% time sink Ian described. Connect the accuracy answer back to their specific pain.

---

## SCORECARD

| Talk Track Element | Executed? | Notes |
|---|---|---|
| Pre-slide discovery opener | ✅ Partial | Asked about AI velocity? No. But did run discovery first. |
| Tech stack question | ✅ Yes | Got clean answer: EKS, New Relic, PD, GitLab |
| Step-by-step process walk | ❌ No | Never asked the full incident lifecycle |
| Tribal knowledge question | ❌ No | Pain was surfaced by prospect but not pulled on |
| "Which use case matters most?" | ❌ No | Never asked; prospect didn't self-select |
| Customer stories woven in | ❌ No | One vague stat, no named stories |
| Evidence grounding demo moment | ⚠️ Partial | Showed the work but didn't frame the "not a black box" differentiator |
| Satellite / security proactive | ❌ No | Healthcare company, never mentioned |
| Locked next step with date | ⚠️ Partial | "Early next week" — no specific day |
| Multi-threading question | ❌ No | Only two SRE contacts, no app/platform expansion |
| "Why" / business driver question | ✅ Yes (Prodan) | Surfaced the 20% productivity OKR — great |
| Budget qualification | ✅ Yes | LP asked directly, got "not planned but not out of scope" |

**Executed well**: 4 of 12
**Partially**: 3 of 12
**Missed**: 5 of 12

---

## TOP 3 COACHING ACTIONS FOR LP + PRODAN

### 1. Pull the tribal knowledge thread — every time
When a prospect says "people don't know what's going on" or "we merged two companies with different processes," that's not a data point to note and move on from. That's the moment to go deeper: *"When one of your TPA engineers gets paged for something they've never seen — what does that first hour look like? Who do they call?"* Then connect it to Resolve's knowledge graph. This call had the setup for a perfect knowledge graph demo moment, and it was missed.

### 2. Pre-load 2-3 customer stories and know when to drop them
LP should walk into every call with Coinbase (incident investigation), Ticketmaster (tribal knowledge), and Veeva (triage time) stories loaded. The rule: when the prospect describes a pain, immediately validate it with a named customer who had the same pain and a specific outcome. *"You said 30% of time on RCA — Coinbase was in the same place. 180-minute MTTR on SEV1s. Now it's 20 minutes."* That's 10 seconds and it transforms the conversation from "interesting tool" to "this is proven."

### 3. Always end with two questions: "who else" and "when exactly"
The call ends warm but vague. Before hanging up: *"Ian, for the re:Invent demo — who else besides your VP should be in that room? Any app team leads or TPA stakeholders who'd benefit from seeing this?"* And: *"For our 1:1 next week — does Tuesday or Wednesday work better? I'll send a calendar hold before we hang up."* Lock it down.
