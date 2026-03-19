---
description: Score current messaging against customer research across 5 dimensions and surface the most impactful gaps
allowed-tools: Read, Write, Glob
---

# Message Gaps Critique

Perform a rigorous critique of current messaging vs. what customers actually say.

## Required Reading

Read ALL of the following before starting the analysis:
- `docs/positioning/` — current messaging (everything in this folder)
- `outputs/research-synthesis.md` — customer evidence (run `/ingest` first if this doesn't exist)
- A sample of raw `docs/interviews/` and `docs/calls/` files for ground-truth customer language

## Two Lists to Build

Before scoring, explicitly build two lists:

**List A — What WE say**: All distinct claims, phrases, and positions in our current positioning docs.

**List B — What THEY say**: All recurring themes, priorities, and language patterns from customer research.

Then compare them systematically across 5 dimensions.

---

## Scoring Rubric (1–5 per dimension)

**5** = Excellent alignment / no significant gaps
**3** = Partial — some alignment but notable misses
**1** = Major disconnect — this dimension needs urgent work

---

### Dimension 1: Language Match (1–5)
Are we using the words customers use, or internal jargon?

Analysis:
- List terms WE use that customers never say (jargon to retire)
- List terms customers use frequently that we ignore (language to steal)
- Give score and 2–3 specific examples

### Dimension 2: Pain Coverage (1–5)
Do we address the pain points customers mention most?

Analysis:
- List the top 5 pains mentioned in customer research (ranked by frequency)
- For each, note: does our messaging address it? Directly, indirectly, or not at all?
- Give score and identify the biggest uncovered pain

### Dimension 3: Outcome Clarity (1–5)
Is it obvious from our messaging what success looks like for the buyer?

Analysis:
- Can someone read our positioning and immediately picture their life after buying?
- Are we describing outcomes or features?
- Give score and 2–3 specific examples of where we describe features when we should describe outcomes

### Dimension 4: Competitive Differentiation (1–5)
Could our messaging apply equally to a competitor? If yes, it's not differentiated.

Analysis:
- Take our top 3 positioning claims. Could [main competitor] say the same thing?
- Which claims are genuinely unique vs. table stakes?
- Give score and flag all undifferentiated claims with [TABLE STAKES]

### Dimension 5: Evidence Credibility (1–5)
Are we making claims we can't back up with customer evidence?

Analysis:
- For each major claim in our positioning, is there supporting customer evidence in the research?
- Flag all unsubstantiated claims with [NO CUSTOMER EVIDENCE]
- Give score and count of unsupported claims

---

## Output Format

Write to `outputs/message-gaps-critique.md`:

```
# Message Gaps Critique
Date: [today]
Positioning docs reviewed: [list]
Research docs reviewed: [list]

## Overall Verdict
[Score: X/25] — [1-paragraph assessment of message-market fit]

## Dimension Scores
| Dimension | Score | Top Issue |
|-----------|-------|-----------|
| Language Match | X/5 | [issue] |
| Pain Coverage | X/5 | [issue] |
| Outcome Clarity | X/5 | [issue] |
| Competitive Differentiation | X/5 | [issue] |
| Evidence Credibility | X/5 | [issue] |

## Detailed Findings
[Full dimension-by-dimension breakdown]

## Priority Action List
Top 5 changes to make, ranked by impact on message-market fit.
Format: [Action] → [Expected improvement] → [Evidence supporting this change]

## Language to Steal Immediately
10 specific customer phrases that should appear verbatim in our messaging.
Each with: phrase, source doc, why it's powerful.
```
