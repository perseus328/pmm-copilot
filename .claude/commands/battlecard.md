---
description: Generate a 1-page competitive battlecard for the sales team
allowed-tools: Read, Write, Glob
argument-hint: "[competitor name, e.g. acme-corp or salesforce]"
---

# Generate Sales Battlecard

Create a 1-page competitive battlecard for: `$ARGUMENTS`

## Pre-Flight

Read `outputs/research-synthesis.md` and `CLAUDE.md`. If the synthesis file doesn't exist, tell the user to run `/ingest` first.

If a competitor name was provided via `$ARGUMENTS`, also look for matching files in `docs/competitors/` (search for filenames containing the argument). Read any matches found.

If no competitor name was provided, generate a general competitive battlecard using the most frequently mentioned competitor in the research synthesis.

## Battlecard Contents

Generate each section using only evidence from actual research documents — no invented claims.

---

**Header**
`[Our Product] vs. [Competitor] | Updated: [date]`
One-line battle summary: "We win when [specific scenario]. They win when [specific scenario]."

---

**Section 1: When You Hear This…**
List 3–4 specific objections reps hear when competing against this competitor.
Source these from call notes and interview docs where possible.
Format each as:
> **They say**: "[objection]"
> **You say**: "[response that pivots to our differentiated strength]"

---

**Section 2: Our Strengths vs. Them**
List 3 concrete differentiated capabilities. For each:
- Capability name
- Why it matters to the buyer (outcome language, not feature language)
- Proof point: customer quote or specific scenario — with source citation

---

**Section 3: Their Real Weaknesses**
List 3 honest limitations of the competitor — only include what customers have actually mentioned. No speculation. Tag each with: Source: [filename].

---

**Section 4: Trap Questions**
2–3 discovery questions that expose areas where we win when the prospect answers honestly.
Example format: "How do you currently handle [X] when [Y situation] happens?"

---

**Section 5: Landmines to Avoid**
1–2 topics to steer away from — areas where we're genuinely weaker. Be honest with your sales team.

---

## Output

Write to `outputs/battlecard-$ARGUMENTS.md` (or `outputs/battlecard.md` if no argument given).

After writing, give the sales rep a 2-sentence briefing on the single most important thing to remember when competing against this opponent.
