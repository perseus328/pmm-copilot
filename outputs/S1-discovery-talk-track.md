# Discovery S1 Talk Track
**For**: First-call deck — Resolve AI
**Audience**: VP Engineering, Head of Platform/SRE, Director of Reliability
**Goal**: Make the prospect feel heard, surface real pain, earn the second meeting
**Tone**: Peer-to-peer, not pitch-y. You're a practitioner who's seen this movie before.

---

## PRE-SLIDE OPENER (Before you show anything)

> "Before I show you anything, I want to ask you something."

> "You've probably rolled out Cursor or Claude or Copilot by now. Your engineers are using it. How is that actually showing up in overall engineering velocity?"

**[Let them respond. Listen for the gap.]**

> "And what are you doing about AI in production today? Anything — homegrown, vendor, or just exploring?"

**[Let them respond. This tells you where they are on the maturity curve.]**

> "What we hear from most engineering leaders is: yes, individual developers feel faster. PRs go out quicker. But the team-level velocity number hasn't moved the way anyone expected."

> "And the reason is pretty simple. AI made the coding faster. But it didn't make running and maintaining that software in production faster."

> "And when we dig into why, it almost always comes back to the same three things."

**[Advance to Slide 3 — Engineering velocity is at risk]**

---

## SLIDE 1 — Title: "AI for Prod"

*Skip or show briefly. This is your cover slide — don't spend time here.*

> "We're Resolve AI. Autonomous alert investigation, collaborative incident remediation, and production debugging. We'll get into all of that — but first I want to understand your world."

---

## SLIDE 2 — "Who are we? Why trust us?"

*Come back to this if needed for credibility, or use it early if the prospect doesn't know Resolve at all. Don't lead with it if they already took the meeting voluntarily — they've done their homework.*

> "Quick context on us: we were founded by the co-creators of OpenTelemetry, with AI researchers from DeepMind and Meta's Llama post-training team. 70+ engineers, all focused on this one problem. $150 million in funding at a billion-dollar valuation."

> "More importantly — we're running in production at Coinbase, Zscaler, DoorDash, Salesforce, and about 20 other complex environments. This isn't a science project. These are real teams using it on real incidents."

*If asked about customer fit:*
> "The pattern we see is: if you have 100+ engineers, a distributed architecture, and your best people are still getting pulled into war rooms — that's where Resolve delivers the most value."

---

## SLIDE 3 — "Engineering velocity is at risk"

*This is your first real slide. It's a tension-builder — you're naming the problem they feel but may not have articulated.*

> "Here's what we keep hearing. On the left side — AI has absolutely accelerated shipping code. Cursor, Claude, Copilot. Your developers are measurably faster at writing software."

> "But on the right side — production hasn't kept up. Reliability. Engineering efficiency. Headcount leverage. The bottleneck has shifted, and it's getting worse because you're shipping more code, faster, into production environments that are just as fragile as they were two years ago."

**DISCOVERY QUESTION:**
> "Is that a pattern you're seeing? More deploys, but incident volume staying flat or going up?"

**[Listen for: deploy frequency, incident trends, MTTR, team size.]**

> "Because what that creates is a tax on velocity. Every outage pulls your engineers out of building mode and into firefighting mode. And that's a direct hit on the thing the board is measuring — how fast are we shipping?"

---

## SLIDE 4 — "Why production needs your attention"

*Now you're getting specific. Three pain pillars. Spend time on whichever one they react to most.*

> "When we break it down, it lands in three buckets."

### Reliability pillar:
> "First — reliability. A customer ticket opens. 10 to 20 engineers are in a war room. MTTR is hours, not minutes. And it's not because your engineers aren't good — it's because the system is too complex for any one person to hold in their head."

*Customer proof:*
> "One of our customers — a large UK financial company — told us: 'Customers act as canaries. They find the problem before we do.' That's the state most teams are in."

**DISCOVERY QUESTION:**
> "When a SEV1 fires at your org, what does the first 30 minutes look like? How many people get pulled in?"

### Engineering efficiency pillar:
> "Second — operational toil. Every alert that fires, someone gets paged. Every page is a context switch. And it's usually your most experienced engineer — the one you need building product — who gets pulled in to figure out what's going on."

*Customer proof:*
> "Veeva's VP of Engineering told us: 'Even for very good engineers, triage still takes them two to three hours. Sometimes six hours depending on the skills of the engineers.' That's not an edge case — that's the norm."

**DISCOVERY QUESTION:**
> "When an alert fires, walk me through what happens step by step. Who gets paged? What tools do they open? How long before they even know what they're looking at?"

### Headcount leverage pillar:
> "Third — knowledge concentration. You hired 10 engineers. Only 2 can actually run production. The rest are months away from being effective on-call. And when one of those senior engineers leaves..."

*Customer proof:*
> "Ticketmaster's SRE lead said it best: 'I would prefer to not use humans as a knowledge base.' That line stuck with us because we hear a version of it everywhere."

> "Veeva told us the same thing: 'An engineer quits, and that knowledge is out the door. It's not documented anywhere. It's 4 to 6 months before a new engineer feels comfortable on-call.'"

**DISCOVERY QUESTION:**
> "When a senior engineer leaves your team — or gets reorged — what happens to that knowledge? Is it documented, or does it walk out the door?"

*This is the #1 most emotionally resonant pain point across 2,000+ calls we've analyzed. Let them talk here.*

> "And all of this is becoming 10x harder with AI-generated code. More code, more services, more ways things can break — but the same number of people to figure out what went wrong."

---

## SLIDE 5 — "Resolve AI for Production"

*Now you're pivoting to the solution. Keep it tight — three use cases, not a feature dump.*

> "So what does Resolve actually do? Three things."

### Incident Investigation:
> "First — when a real incident fires, Resolve investigates autonomously. It pulls logs, metrics, traces, recent deploys, and correlates across your entire stack. It doesn't just surface one signal — it reasons across multiple layers to find root cause. And it shows every step of its work with cited evidence."

> "This isn't a chatbot. It's an agent that does the investigation your best engineer would do — checking hypotheses, critiquing itself, grounding every claim in your actual data."

*Customer proof (weave in Coinbase):*
> "At Coinbase, this cut major incident investigation from 2 hours down to 20 minutes. And the team told us: 'By the time I get to my desk, Resolve already has it.' That's the shift — from reactive scrambling to the work being done before you even open your laptop."

### Alert Triage:
> "Second — alert triage. For the hundreds of alerts that fire every day that aren't incidents, Resolve handles the triage. Engineers only see what actually needs their attention. The rest gets investigated, contextualized, and resolved — or flagged as noise."

> "That kills the operational toil that's stealing your best engineers' time. They focus on product, not on-call."

### Production Work:
> "Third — production debugging for everyone. Resolve becomes how any engineer reasons about production, not just the two senior people who 'know the system.' It democratizes that institutional knowledge."

> "As one of our reps put it to Vonage: 'Resolve takes your smartest engineers and disseminates whatever they're doing to even the most junior engineers. It uplevels everyone.'"

**DISCOVERY QUESTION:**
> "Of these three — incidents, alert triage, production debugging — which one would move the needle most for your team right now?"

*This question does two things: it qualifies the entry use case, and it lets the prospect self-select what matters most.*

---

## SLIDE 6 — Coinbase Customer Story

*This is your proof point. Tell it as a story, not a data dump.*

> "Let me give you a concrete example. Coinbase."

> "Before Resolve: 160 Kubernetes clusters, 200+ engineering teams, billions of log lines daily. When a SEV1 or SEV2 hit, MTTR was 180 minutes. Engineers were manually triaging across Datadog, PagerDuty, logs, traces, and runbooks — most of which were stale. Only senior engineers could navigate the complexity. Everyone else waited for someone who 'knows.'"

> "Sound familiar? [Pause.]"

> "Here's what the rollout looked like. We started in shadow mode — zero noise, zero disruption. Resolve watched incidents and generated hypotheses alongside the team. Engineers saw it getting things right. Then something interesting happened — teams started pulling Resolve in themselves. Organic adoption. About 3 teams onboarded every 2 weeks, no top-down mandate."

> "The impact: 60% faster root cause detection. Major incidents down from 2 hours to 20 minutes. User-initiated investigation chats up 200%. Active users up 94%. 206 engineers using it today — and they're scaling to 400+ company-wide."

> "And here's the quote that matters most: 'Gets work done 95% of the time. By the time I get to my desk, Resolve already has it.'"

**DISCOVERY QUESTION:**
> "When you think about rolling out a tool like this — would your team respond better to a top-down mandate, or would it need to prove itself organically?"

*This tells you about their change management culture — critical for POC scoping.*

---

## SLIDE 7 — "How Resolve Works" (Markitecture)

*Keep this conversational. Don't read the architecture diagram — explain the "so what."*

> "Architecturally — Resolve connects to your existing stack. Infra, observability, codebase, knowledge bases. We're not asking you to rip and replace anything."

> "What makes us different is what sits in the middle. Post-trained models — not generic LLMs, but models specifically trained on production troubleshooting data. A memory system that learns your environment over time. Multi-agent architecture so Resolve can reason across logs, metrics, code, and deploys simultaneously."

> "And there's a continuous improvement loop. Every investigation, every piece of feedback, makes the system better for your specific environment."

**If they ask about data security:**
> "We support satellite deployment — Resolve runs inside your VPC, your data never leaves your environment. For regulated industries — financial services, healthcare — that's typically non-negotiable, and we built for it from day one."

**DISCOVERY QUESTION:**
> "What does your observability stack look like today? Datadog, Splunk, something else? And how many tools is a typical engineer switching between during an incident?"

*Wells Fargo's Prasanth described this perfectly: "A typical flow runs through multiple ops — 5, 6 ops, hitting 10 different microservices, hitting another set of microservices, all the way to mainframe and third-party systems." If your prospect has similar complexity, mirror that back.*

---

## SLIDE 8 — Demo

*Before you click into the demo:*

> "I want to show you this working on a real scenario. But before I do — is there a specific type of incident or alert pattern that would be most relevant for your team to see?"

**[Let them shape the demo. This is a discovery moment disguised as a demo setup.]**

> "Great. Let me show you what this looks like end to end."

*During the demo, call out two things explicitly:*

1. **Evidence grounding:** "See how every claim has a citation? Every data point links back to the actual log line, metric, or deploy that Resolve used to reach that conclusion. This isn't a black box — your engineers can audit every step."

2. **Self-critique:** "And notice this — Resolve isn't just taking its first theory. It's checking alternatives, critiquing its own hypothesis. That's what separates it from a chatbot that anchors on the first signal it sees."

*Customer proof to drop during demo:*
> "This is actually the feature that gets the strongest reaction from technical evaluators. Abridge's engineering lead told us their biggest concern with AI in prod is 'a small tune in the prompt can completely crush it — it'll break some cases that used to work.' That's why we built the eval loop and evidence grounding — so you can see exactly what changed and why."

---

## SLIDE 9 — "Where AI for Prod is heading in 2026"

*Use this as a vision slide — where the category is going, not just where Resolve is today.*

> "Looking ahead — here's where we see this going in 2026 and beyond."

> "Today we're delivering investigation and triage. Next: automated remediation — Resolve generates PRs and executes fixes with safety guardrails and human approval. Proactive optimization — spotting reliability patterns before they become incidents. Automated reporting — from SLO reports to on-call handovers. And enhanced teachability — the system evolves from every interaction."

> "The key idea is: Resolve isn't a point tool. It's a platform that gets smarter the more your team uses it."

**DISCOVERY QUESTION:**
> "If you could wave a magic wand — what's the one production workflow you'd most want to automate or eliminate?"

---

## SLIDE 10 — Next Steps

*This is where you close for the second meeting. Be specific.*

> "So here's what we'd suggest as next steps."

> "First — a deep-dive technical demo. We'll show Resolve working against a scenario that looks like your environment. Not canned — real."

> "Second — let's lock down 2-3 use cases that matter most to your team. We define success criteria together before anything starts."

> "Third — if you're in a regulated environment, we can kick off the security review in parallel. We support satellite deployment, SOC 2 Type II, and we've been through this with BlackRock, JPMC, and others."

> "And fourth — share your integration inventory. Tell us your stack, and we'll map which integrations matter most for your use case."

**CLOSING QUESTION:**
> "Based on what you've seen today — does this feel relevant to what your team is dealing with? And who else on your side should be in the room for the deep-dive?"

*The second question is critical. If they say "just me," you may be in the SRE trap — one engaged champion who can't drive the deal alone. If they name specific people, you've opened the multi-threading.*

---

## APPENDIX SLIDES — Use if needed

### "Why is this such a hard AI problem" (Slides 13-16)

*Use this if the prospect is technical and skeptical, or if they bring up build-vs-buy.*

> "Let me address the elephant in the room. Why can't you just build this with Claude or Cursor?"

> "It's a totally fair question. And the answer is: you can get to about 50% accuracy pretty quickly. The first 50% is easy — hook up an LLM to your logs and metrics, give it some tools, and it'll do shallow reasoning on straightforward issues."

> "The problem is the remaining 50%. That's where all the hard engineering lives."

*Walk through the five barriers:*

> "One — accuracy under pressure. In a code editor, a wrong suggestion costs you 30 seconds. In production during a live incident, a wrong autonomous action makes things worse. The model has to be right — not 'pretty good,' actually right — in the moments that matter most."

> "Two — multiplayer. Production issues don't happen in a terminal. They happen across Slack threads, incident channels, multiple teams, all moving fast. The AI has to coordinate with humans and other agents in real time."

> "Three — autonomous and steerable. When to act, when to ask, when to say 'I need more context.' Getting that judgment right for your specific environment takes deep research and fine-tuning."

> "Four — tool use in your context. Knowing that Datadog exists isn't the same as knowing how your team queries logs, which dashboards matter, what a normal error rate looks like for your topology. That context layer is non-trivial to build."

> "Five — models change. You build something on Opus 4.5, six months later there's a new model, behavior shifts, regressions happen. Most teams can't afford to treat their AI ops tooling as a product that needs constant iteration."

**DISCOVERY QUESTION (if build-vs-buy comes up):**
> "Have you started building anything internally for this? How far did you get, and where did it plateau?"

*This is a qualifying question. If they say "we built a Slack bot that reads alerts," that's the 50% ceiling. If they say "we have a team of 5 working on it," that's a different conversation — you're competing with internal engineering, and the message needs to be about the eval loop, post-trained models, and accumulated production incident training data they can't replicate.*

### Road to AI for Prod (Slide 12)

*Use this to place the prospect on the maturity curve and frame the conversation around progression, not replacement.*

> "We think about AI for production as a maturity journey. Most teams start at manual triage — on-call, alert-by-alert, all human. Some have moved to traditional automation — prescriptive runbooks, if-then logic."

> "The next step is AI assistants — Claude, Cursor, tools that help individual engineers. That's where most teams are today."

> "What we're building is the next two stages: autonomous agents that plan, investigate, and act — and eventually, agent teams that collaborate with humans and each other."

> "Coinbase started at stage 3 and is now moving toward stage 4. Whatnot started their POC at stage 3 and within a few months reached 80-86% accuracy on autonomous investigations."

**DISCOVERY QUESTION:**
> "Where would you place your team on that curve today? And where do you want to be in 12 months?"

---

## REP COACHING NOTES

### Discovery questions ranked by impact (use the top 3 every call):

1. **"When a senior engineer leaves your team, what happens to that knowledge?"** — Opens the tribal knowledge conversation. Universal pain, high emotion.

2. **"Walk me through what happens when a SEV1 fires. Step by step, from alert to resolution."** — Surfaces process pain, tool fragmentation, and team dynamics.

3. **"Of incidents, alert triage, and production debugging — which would move the needle most?"** — Qualifies entry use case without you choosing for them.

4. **"Have you started building anything internally for AI in ops? Where did it plateau?"** — Qualifies build-vs-buy and positions Resolve as the next step, not a competitor to their internal work.

5. **"Who else on your team should be in the room for the deep-dive?"** — Multi-threading. If they say "just me," flag the SRE trap risk.

6. **"Would your team respond better to a top-down mandate or organic adoption?"** — Change management intelligence for POC design.

### What NOT to do:
- Don't jump to the demo before discovery. The best reps in our data run 15+ minutes of step-by-step process questions before showing anything.
- Don't lead with pricing or packaging. If it comes up, defer: "Let's figure out what moves the needle for your team first — we'll make the commercial side work."
- Don't let "let me run it by my manager" be the last thing said. Always lock a specific date: "Great — when would that conversation happen? Can I send a one-pager they can review in advance?"
- Don't sell to a single SRE. If the only champion is one SRE lead, ask: "Who owns the budget for tooling like this? And who on the app or platform side would benefit from seeing this?"
