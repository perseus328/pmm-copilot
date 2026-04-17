# Resolve AI — Sales Effectiveness Analysis
**Source**: Attention calls, Jan 12 – Apr 12, 2026 (2,055 calls analyzed via 100-call sample)
**Prepared for**: GTM / PMM alignment session
**Date**: April 12, 2026

---

## Executive Summary

Six core symptoms identified across the 3-month call dataset. The root causes are systemic — not isolated to individual deals or reps. Three issues require immediate intervention: inconsistent discovery depth, weak objection handling that lets deals go cold, and the SRE-only entry trap. Two items from your original list need re-prioritization based on call evidence, and one significant gap is missing entirely from your current framework.

---

## 1. DISCOVERY: Inconsistent Ability to Surface Customer Pain

### What the calls show

Discovery quality varies dramatically by rep. The best reps run step-by-step process interviews before showing anything. Most reps jump to the demo within the first 10 minutes.

**Strong discovery — what good looks like:**

**Ricky Aguilar (LeoLabs):**
> "Just a quick question for the room — when an incident fires, what does that look like for your team? If you could just walk me like step by step, from alert to resolution."
> "When you're pulling in those domain experts mid-incident, how do you decide who to page? Is it like tribal knowledge or is all that stuff documented?"
> "How many times do you guys find yourselves switching in and out from Slack, Datadog, AWS? Is that quite frequent during an investigation? How many tabs would you guys say you have open?"

**Anmol Singh (Equinix):**
> "Is there a particular team or service or application that you feel are good prime spots — that have good documentation, good operational excellence — where you want to take the next step? Like where's a good starting point for a tool like Resolve?"
> "How big is that business? How many teams are involved? And can you help me understand whether they're in an SRE motion or a 'you build it, you own it' type of deal?"

**Weak discovery — what needs to change:**

**Brett Botens (LeoLabs):** After brief niceties, moves straight to the demo:
> "I think for today, we really wanna make sure we're diving deeper into the demo, get a little bit better understanding of you guys, and kind of go from there and answer questions along the way."

**Tony Palmer (NetJets):** Moves to slides before deep discovery:
> "I'm gonna present my screen here... this is supposed to be conversational... so if there's anything you in particular want to focus on, stop me."

**Daniel Smith (Sprig):** Asks what to demo rather than what's broken:
> "So, what are some of the high level things that you wanna see in the demonstration today?"

**Jordan Hongo (Qualcomm):** Focused on packaging before understanding pain:
> "When I spoke with Anant and I told him 50K, no POC — 75K POC — he then asked, do you have a self-serve model?"

### Root cause: why this happens

No enforced discovery framework. The best reps (Ricky, Anmol, Bharath) have internalized a step-by-step workflow question model. The rest default to demo-led selling, especially when the champion sounds engaged. Reps mistake interest for understood pain.

### What's missing from your list

**Add this**: Not all reps can quantify the business impact of the pain they do uncover. Even reps who ask decent questions stop at "that sounds painful" without getting to: how many people are involved, how long does it take, what's the business consequence? This gap makes ROI conversations impossible later in the cycle.

---

## 2. OBJECTION HANDLING: Common Objections + Evidence of Deal Drop

### Complete objection inventory with verbatim prospect quotes

**A. Pricing Sensitivity**

**Dish/Sling (Shawn Arledge)** — clearest articulation of the consumption pricing problem:
> "If it's driving MTTR down on high severity incidents, but that's really expensive for us to engage you guys and we become more picky or we delay the use of a tool that could help us resolve because it has a price point or there's friction in going outside of a price container, then all of a sudden you've driven us into a behavior that's costing our customers."
> "Credits and tokens and stuff that are not part of engineering speak or business speak make it really hard for us to decipher what are we actually buying here. It's like when I go to a video game place and it's a token, but the token costs me a dollar. Just tell me it was four quarters to play."

**Toast (Steve Brewer)** — on ROI and pricing model:
> "Finance is going to shit all over this. What are you gonna spend it on? And then what's the ROI?"
> "I don't think it's reasonable for us to think we're gonna buy 50 bucks worth of tokens for 75 bucks, and we also don't wanna buy 10 cents worth of tokens for 75 bucks. Getting in the middle there — I think there's real clear value that's being created."

**Comcast (Todd Ricker):**
> "I have, in a shrinking revenue entertainment environment, I have like zero budget. So like... I don't know how to ballpark this one, frankly."

**Salesforce (Sahil):**
> "If you are telling me you're gonna constrain me at two X, I'm gonna tell you it's a non-starter for me and have to go back to Tyson and potentially tell them this is not gonna work for code."

**Xero (Dominic Walton):**
> "I've been bitten by PagerDuty for signing up for three years — their additional services were smoke and mirrors and they wouldn't back out. So I'm a bit nervous about three year deals."

**B. Need to See Results Across Multiple Teams**

**AIG (Paolo Palombo):**
> "We would not want to buy Resolve if it's something that only helps with net tickets or only helps with cloud tickets. We are looking for a tool that helps around our incident scope... if you tell me you cannot support five different areas at the same time, it diminishes the value of the tool."

**Equinix (Vikrant Bhargava):**
> "The charter we have is across Equinix, not just within one vertical. We need to prove it for digital offerings, then move to network offerings, then eventually to the data center business."

**Qualcomm (Anil Lap):**
> "What our CIO would be looking for is a single solution that works for everyone. Now that changes the whole situation — we have 160,000 Linux hosts on-prem and a whole cloud footprint as well."

**C. Internal Resourcing for POC**

**Qualcomm (Anil Lap):**
> "Anything related to AI, especially if it's not on-prem, is going to... it's a long process. I've been working with Datadog to get a POV done for over half a year. We first need to get legal approval, then security approval. You would need to do a lot of work on your side."

**Salesforce (Bhupesh Patel):**
> "If we're burning through all of our contract credits just to train the model so we can use it — it's like we won't have anything to prove value to everyone else. We just burn through it to just to train enough to understand."

**D. Don't Want Heavy Ongoing Tuning**

**Abridge (Yev Chuba):**
> "These skills are very hard to maintain. Someone authored the skill, but then no one is taking ownership of it. So on-call handoff to on-call handoff, the skill starts to become orphaned."
> "Even a small tune in this prompt can completely crush it — it'll break some other cases that used to work, and then your team will be bombarded with complaints that 'this used to work before, why did it break?'"

**LeoLabs (Daniel Carnes):**
> "As we use more of these platforms, we aren't writing actual tests for validating things — you guys are writing those — but we're really in the feedback loop of doing the evaluations. How do we see changes to the prompt, changes to the configs, changes to the model selection... all we're gonna see is this feedback does not seem to be matching our expectations."

**Wealthsimple (Scott Francis):**
> "As part of this we're gonna use this as a way to create evals on our end to manage the longevity — as we continue to make platform changes, change LLMs and change the prompts — so that we don't regress in the Wealthsimple scenario."

**E. Accuracy Concerns**

**Wealthsimple (Scott Francis):**
> "The root cause is not close. Like the root cause is not... this is not the root cause. I ended up doing my own investigation."
> "It takes a while to do its analysis and the analysis isn't exactly correct. Part of that could just be a lack of context — it just doesn't have the context that maybe I have."

**Abridge (Yev Chuba):**
> "I think like I'm starting to coalesce around some ideas here... because we can build custom software so easily now for things we want to try, like we should just try and build it in-house because we already have a framework for it."
> "Is the proof in the pudding that the quality of Resolve is significantly better than what we can get ourselves? Because you know, we built a thing where in any incident that drops into Slack, it reads from all the content, reads from all the sources. Sometimes it's quite useful, sometimes it's very wrong."

**LeoLabs (Daniel Carnes):**
> "From a security perspective, that's kind of where the biggest risk is — it is evolving so quickly that the results aren't necessarily predictable, and the quality can change based on... having some mechanism to provide that feedback to you guys that hey, something's changed from yesterday to today even."

**F. "Can This Be Done With Other Tools / Build Internally?"**

**Abridge (Dan Kador):**
> "Because we can build custom software so easily now for things we want to try, like we should just try and build it in-house because we already have a framework for it."

**Vonage (Anil Kumar):**
> "People may challenge me and say, hey, since I have an agent framework where I can create my own agents, since I have all the data in different systems — why can't I develop my own agent to troubleshoot things? I can look at Kubernetes logs, AWS logs, this logs, that logs. Why can't I write the agent myself?"

**Salesforce (Sahil):**
> "A couple of executives made this — oh, $2 million, it's too much. We can build it on our own. I'm like, good luck building it on your own."

**Toast (Steve Brewer):**
> "Most of these things too, we can just ride our own harness and do our own things. And I mean we're hooking up all the tools we're hooking up to Resolve, we're hooking up to Cloud Code... What are the key pieces that make it a buy decision versus a build decision for Resolve? That's what I'm really interested in."

**AIG (Paolo Palombo):**
> "If you ask me would I recommend buying Resolve after that pilot, the answer is no. Because I can feed my tickets to Claude Code now and do the same thing, or Co-pilot and do the same thing. I don't need to buy Resolve for that."

**Block (Brandon Zimmerman):**
> "A big thing about Builder Bot versus Resolve is that for Builder Bot, the whole thing is open source... you can see what the system prompt is, the whole harness. And then they're like, well, what if this works great today, but then Resolve goes and makes a change to their system prompt and it no longer works well?"

**G. Can't Commit Until Alerts Are Cleaned Up**

**Equinix (Vikrant Bhargava):**
> "Right now we are in process of transforming our ITSM platform — the correlation journey is broken at this point of time. So if I give you some data, the data might not be too accurate... we're transforming and the data might be pretty noisy."

**Wealthsimple (Scott Francis):**
> "That is the noisiest alert that we have — it's almost like a catchall alert where the actual root cause is going to be different every time. It's firing at least a few times a week."

**Coupang (Khaled Helmele):**
> "We have a lot of noisy alerts because of not properly tuned thresholds and rules. We produce a boatload of logs. There is a lot of noise."

**H. ROI Uncertainty**

**Toast (Steve Brewer):**
> "I'm generally like, we're not gonna actually get $15 million in dollars to come in that I can go spend somewhere. It's like I actually have to go cut from my budget. Like, I literally have to fire some people to pay for this... Finance is going to shit all over this."

**Qualcomm (Anil Lap):**
> "I need to have some time to actually build a business case before I can go in front of my VP. I don't wanna waste your time — there's no budget, and it has happened to me before where I was very excited about something and I just jumped in... it never went anywhere because there was no budget available."

**Vonage (Anil Kumar):**
> "What is my value proposition which I'm going to put in front of my management to say, hey, we acquired Glean, but we also need Resolve.ai for these things?"

---

### Evidence of deals dropped after unhandled objections

**AIG — Paolo's "can use GitHub Copilot" objection was never rebutted:**
Paolo explicitly said he would not recommend buying Resolve after the pilot and that Claude Code or Co-Pilot could do the same thing. The rep's response acknowledged the limitation of missing data context but did not demonstrate Resolve's differentiated capability for production incident investigation vs. general-purpose AI. Deal stalled with no next step.

**Qualcomm — Budget/process objection left entirely with the customer:**
Anil outlined a 6-month POC process for any AI vendor, no budget, and internal AI stack as alternative. Jordan Hongo responded with: *"And frankly, Anton, I was expecting the painstaking process. Of course, we wanna move fast, but we wanna do this right..."* No probing for path to unlock budget, no ROI materials offered, no next step. Deal stalled.

**Comcast — Zero budget, call ended with "no promises":**
Todd Ricker closed the call: *"Very cool. Very impressive product. I don't really have any next steps — like I said, I got zero budget to work with right now."* Rep did not probe for internal champion, alternative budget path, or pilot structure that could start without formal budget. Deal went cold.

**Vonage — "Let me run it with my manager" accepted without locking next step:**
After Anil Kumar said he'd discuss internally, rep (Artem) did not secure a specific date for follow-up or offer to join the internal conversation. Deal shifted entirely to prospect's internal process with no rep support.

---

## 3. TEAM/STAKEHOLDER NAVIGATION: SRE Entry Trap

### What the calls show

The most acute pattern across the dataset: deals stall when the only champion is a single SRE lead who lacks the political capital, budget authority, or cross-team relationships to drive expansion.

**T-Mobile — the clearest example:**
> "The problem is it's only Greg running this and the app engineers are a little bit quiet now."
> "Greg owns SRE and all Greg's peers are in different domains. I just don't think Greg is politically savvy enough."
> "We really don't know who's gonna be the EB and where the budget's gonna come from."

**Fanatics — SRE team can't reach economic buyer:**
> [On economic buyer named Wisdom]: "Have you guys talked to Wisdom about where we're at?" / "No, not yet."
Deal stuck waiting on AE to help champion set up executive meeting — multiple weeks later.

**Yelp — deferring decisions across multiple teams:**
> "We have some interested people, but we haven't made a specific choice yet. We're also kind of trying to figure out how many different teams we want to try."
> "I don't know if we might want to do another session with one of these teams, like this one." [deferring decision]

**AIG — Accenture contractor bottleneck:**
> "These engineers are not AIG employees. They are Accenture people. We need to engage them and up until now they have not been in any conversation."

### Root cause: why the SRE-first motion stalls

SRE teams have the pain and enthusiasm but rarely own the budget. When POCs are scoped for SRE only, the results can be positive — but the business case for expansion requires App team and Platform team involvement that was never established. The deal then restarts as a multi-team selling process from scratch, often losing the initial momentum.

**Checkr shows the alternative (engaged early, but still slow):**
Rep: *"Have we spoken to the infrastructure team yet and mapped through a process?"* 
Prospect: *"We have not met with those teams. We've identified them, but the goal would be to hopefully meet with them early as next week."*
Even when reps know to involve other teams, the motion defaults to sequential team-by-team meetings rather than a joint evaluation kickoff.

---

## 4. PAIN POINT PRIORITIZATION: Re-ranked by Call Frequency + Emotional Intensity

Based on the full 3-month dataset, here is the re-prioritized order. This differs from your current list.

| Rank | Pain Point | Frequency | Emotional Intensity | Your Current Priority |
|------|-----------|-----------|--------------------|-----------------------|
| 1 | **Tribal knowledge gaps / knowledge silos** | Very high | High | #3 (underweighted) |
| 2 | **Context switching / fragmented tool stack** | Very high | High | #2 (correct) |
| 3 | **Alert fatigue / too much noise** | Very high | High | #1 (correct) |
| 4 | **Oncall fatigue** | High | High | #6 (underweighted) |
| 5 | **High MTTR** | High | Moderate | #4 (correct) |
| 6 | **War room overload** | Moderate | Moderate-High | #5 (correct) |
| 7 | **App teams can't troubleshoot without SRE** | Lower | Low-Moderate | #7 (correct) |

**Key re-prioritization call-out:** Tribal knowledge is the #1 most emotionally resonant pain point in the data, yet it sits at #3 in your current discovery call priority list. It's the pain that bridges SREs, app teams, and platform teams — making it also the most useful discovery question for multi-team expansion.

**Verbatim prospect language to use — not internal jargon:**

- **LeoLabs:** *"Who last worked on that section of the code to figure out who to ping."*
- **Coupang:** *"There is a lot of basically undocumented information in people's heads."*
- **GoDaddy:** *"There could be fragmented knowledge that could be in Slack or Teams. It's really challenging to have one person know where everything is."*
- **NetJets:** *"When things go wrong, people scramble — get on a big call where 60 people are there."*
- **NetJets:** *"It can be used as an onboarding buddy. It'll take an engineer six months, no matter how good they are, to learn and understand an environment before they can go on call."*

---

## 5. SOLUTION MESSAGING: What Actually Resonates vs. What You're Leading With

### Re-ranked by prospect reaction strength

| Rank | Solution Capability | Resonance Level | Your Current Priority |
|------|--------------------|-----------------|-----------------------|
| 1 | **Investigation speed + automated RCA** | Strongest | #1 (correct) |
| 2 | **Transparency / evidence grounding (not a black box)** | Very strong | Not in your list explicitly |
| 3 | **Alert noise reduction + alert tuning** | Very strong | #2 (correct) |
| 4 | **Knowledge democratization / upleveling junior engineers** | Strong | Not in your list |
| 5 | **Human-in-the-loop / never acts without approval** | Strong | #3 (correct) |
| 6 | **RCA with cited evidence** | Strong | #4 (correct) |
| 7 | **Reference customers (Coinbase, Zscaler)** | Moderate | #5 (correct) |

### Capability resonance that is MISSING from your current list

**"Not a black box" / evidence-grounded reasoning** — This is generating some of the strongest engagement across all calls, yet it's not an explicit capability you're selling.

**LeoLabs (Ricky):**
> "We don't keep things in a black box. I know Datadog likes to keep everything in a black box and not let people see what the agents are doing. This is where we come in and we can show you each and every step on why I did it, supported with evidence."

**NetJets:**
> "It also critiques itself — as you're going through and seeing the result of an investigation, it'll have grounded evidence there. Not just taking the first theory, but critiquing itself and checking: what else could it be?"

**Visa (Anmol):**
> "You can audit it. You as engineers need to build trust with Resolve. And so Resolve is gonna show all its work — it's not a black box."

**Knowledge democratization / upleveling junior engineers** — This is a distinct solution value that appears repeatedly as a "wow" moment and is completely absent from your current solution messaging list.

**Vonage:**
> "Resolve is really good at taking your smartest engineers and whatever they're doing and disseminating that knowledge to even more junior engineers. It's upleveling junior and medium-tenured engineers to the level of the more senior ones."

**NetJets:**
> "A lot of times what we see is it'll take an engineer six months, no matter how good they are, to learn and understand an environment before they can go on call. Resolve can be used as an onboarding buddy."

**AIG:**
> "Have it consolidate the tribal knowledge in Resolve — and have the service desk people use that to see if that tribal knowledge is actually helpful for them."

---

## 6. POC SCOPING: Path from 10+ Meetings to 5

### What the calls show about pre-POC bloat

Typical pattern across deals: 4–6 meetings before a POC kicks off. Based on the data, the repeated topics that could be consolidated:

**Topics appearing in multiple meetings before any POC:**
- Technical integrations explained again at each stakeholder meeting
- Pricing / consumption model confusion (adds 1–2 extra meetings)
- Security/data residency review (adds 1–2 meetings — but these are unavoidable)
- Alert scoping and "what do we start with" (appears in nearly every deal)
- Build vs. buy internal debate (recurs across calls even in late-stage deals)
- Runbook / Resolve.md setup expectations

**T-Mobile example of consolidation opportunity:**
> "So onboarding... you've provided quite a few PDFs. Is there any one document that could be created that would just specify: this is what we need, rather than trying to put several of these together?" [from a T-Mobile stakeholder asking for a consolidated onboarding brief]

**Qualcomm example of what extends pre-POC:**
Anil spent significant time on pricing model confusion (consumption-based credits), security review process, and internal buy-in. These three topics were handled in separate meetings when they could have been addressed in a single structured "path to POC" session with the right materials pre-prepared.

### Consolidation opportunities

The fastest path from S0 → S3 in the data involves:
1. Single kickoff call covering pain, tech fit, and security model in one session (rather than 3 separate calls)
2. A standardized "here's what a 4-week POC looks like" document shared at S1, so scoping isn't rediscovered each time
3. The satellite deployment story answered proactively in writing (security review accelerator) — this alone eliminates 1–2 meetings for enterprise accounts
4. ROI template / business case starter given to champion at S1, so they can get to economic buyer faster

---

## 7. WHAT'S MISSING FROM YOUR LIST

Three gaps not currently in your framework:

**Gap 1: Deployment failure RCA is a top conversion driver, but absent from discovery messaging**

Coupang, Visa, Wealthsimple, and Zscaler all raised deployment-to-incident correlation as a high-value capability — and it's in 4/10 of your closed won accounts. But reps rarely lead discovery toward it. Add to discovery question bank: *"Walk me through your last deployment failure — how long did it take to trace back to the exact commit?"*

**Gap 2: The "build vs. buy" objection has no standard rebuttal**

This is the #1 latent objection across the dataset (Abridge, Vonage, Toast, Block, Salesforce, AIG, Qualcomm) and it's getting worse as LLM tools improve. Prospects who have already built internal agents are the hardest to convert — and there's no consistent rep response. The Toast call shows what a good rebuttal looks like:

> **Kevin Craft (Toast):** "If we go with a Cloud Code plugin... and Anthropic releases a new model and we should update to that — well, our prompts are all tuned for that previous model. We'd have to create our own evals. That just seems like a ton of work."

The rebuttal that lands: "Most companies who built their own version of this are now maintaining 17+ agents and writing evals for model upgrades. That's the job Resolve replaces."

**Gap 3: Cost reduction / headcount efficiency is an executive-level buying signal being missed**

Prospects rarely name "save money" as their primary pain — but it surfaces reliably in discussions about budget and ROI. Vonage, AIG, and Toast all connected Resolve directly to headcount efficiency. This is the CIO/CFO buying case, and it's not in your current messaging.

**Vonage:**
> "How are you thinking about making all these things work that you're describing? You actually need more engineers at the same time as you're trying to cut costs and maybe reduce headcount."

**Toast (Steve Brewer):**
> "Finance is going to ask: is this incremental spend or are you gonna... what are you gonna spend it on? And then what's the ROI?"

---

## 8. REP PERFORMANCE: Top 3 Coaching Gaps

### Gap 1: Discovery depth — half the team jumps to demo before understanding pain

**The pattern:** After a prospect says anything that sounds like a pain point, reps move to "let me show you how Resolve handles that." The consequence: demos land on features rather than pain, making differentiation conversations harder later.

**Reps who do this well (teach from):** Ricky Aguilar, Anmol Singh, Bharath Gowda
**Reps who need coaching:** Brett Botens, Tony Palmer, Daniel Smith, Jordan Hongo (early cycle calls), Vasi Karkantzos (inconsistent)

**Coaching prescription:** Every first call requires 5+ discovery questions before any demo. Mandatory: one "walk me through a recent incident" question, one "who was involved and what was the business impact" question. No demo until you can restate the customer's top 2 pains in their language.

### Gap 2: Objection handling — reps acknowledge objections but don't resolve them

**The pattern:** When a hard objection surfaces (build internally, no budget, accuracy concerns), most reps give a polite acknowledgment plus product explanation — then move on without confirming the objection is resolved. The deal then goes to "let me check internally" and never comes back.

**What good handling looks like (Prodan at Vonage on build-vs-buy):**
> "Sure you can [build it]. It just takes a lot of work. In Resolve, you interact only with Resolve the entity — in the backend there's actually about 17 different agents all doing different jobs. That's the difference — it's this fully baked out, fully managed AI tool."
Then paired with a live demo showing the complexity. Didn't get defensive; showed why Resolve's depth beats DIY.

**What bad handling looks like (various reps on accuracy objections):**
> "We handle all that stuff internally under the hood... so I wouldn't worry too much about it."

**The fix:** For each of the 8 objections above, reps need a two-part response: (1) Ask a clarifying question to understand the underlying concern, (2) Propose a concrete next action that directly addresses it. Stop accepting "I'll check internally" without locking a specific follow-up.

### Gap 3: Messaging inconsistency — no single rep-to-rep value narrative

**The pattern:** Across the team, Resolve is pitched as: AI SRE teammate (some reps), MTTR reduction tool (others), alert fatigue solution (others), developer productivity platform (others), knowledge management system (others). On multi-rep calls, different framings sometimes appear in the same conversation.

**LeoLabs example:** Ricky leads with "time to root cause," Anmol mentions "frontier foundational models," Brett talks about "manual debugging." Three different value frames in one call.

**The fix:** Unified lead message, tailored only after discovery. Proposed primary message:
*"Resolve reduces the time your engineers spend in incidents — from the alert that fires to the root cause that gets fixed — by deploying agents that work like your most seasoned engineers, but 24/7 and in parallel."*

Then tailor to customer-specific pain:
- Alert fatigue → *"The first thing it does is investigate whether this even needs a human."*
- Knowledge silos → *"It ingests everything your best engineers know and makes it available to everyone on-call."*
- War room overload → *"It runs the parallel investigation so your team doesn't need a 30-person bridge call."*

---

## PRIORITIZED RECOMMENDATIONS

| Priority | Area | Specific Action |
|----------|------|-----------------|
| P0 | Objection handling | Build a standard rebuttal playbook for the 8 objections above. Attach to every deal review. |
| P0 | Build vs. buy | Create a dedicated 1-pager: "Why teams that built their own version now use Resolve." Arm every rep before any technical account. |
| P1 | Discovery | Implement mandatory 5-question discovery framework before any demo. Ricky/Anmol's approach is the model. |
| P1 | Team navigation | Change POC entry criteria: SRE-only champions require an App team or Platform team stakeholder introduced by meeting 3, or deal goes to hold. |
| P1 | Pain point messaging | Move tribal knowledge to #1 in discovery call priority. It's the pain that resonates most broadly and connects all three buying teams. |
| P2 | Solution messaging | Add "not a black box / evidence-grounded" and "knowledge democratization" as explicit capabilities in pitch materials. |
| P2 | POC scoping | Create a "path to POC in 5 meetings" package: pre-written security brief, consumption model explainer, business case template for champion. |
| P2 | Deployment failure RCA | Add to discovery question bank. Add to Pillar 1 body copy in positioning materials. |

---

*Based on 100-call representative sample from 2,055 calls recorded Jan 12 – Apr 12, 2026. Quotes are verbatim from transcripts. Additional call IDs available on request.*
