---
description: Generate 7 homepage headline and subheadline options with evidence tags and tone variety
allowed-tools: Read, Write
---

# Generate Homepage Headlines

Generate 7 distinct homepage headline + subheadline pairs.

## Required Reading

Before generating, read:
- `outputs/research-synthesis.md` — customer language bank and verbatims
- `docs/positioning/` — current positioning to reference and improve on
- `CLAUDE.md` — product context and ICP

If `outputs/research-synthesis.md` doesn't exist, tell the user to run `/ingest` first.

## Headline Rules (Apply to Every Option)

1. Lead with the **outcome**, not the feature
2. Name the buyer's world — reference their reality, not your product
3. Headline: 10 words or fewer
4. Subheadline: 20 words or fewer — adds the "how" or "for whom"
5. Each option must be **distinctly different** — not just a one-word variation of another
6. Use customer language from the research synthesis wherever possible
7. Every option must include an [EVIDENCE] tag citing the source doc or verbatim it draws from

## Tone Coverage (Across the 7 Options)

| # | Tone | Description |
|---|------|-------------|
| 1 | Outcome-led | What life looks like after buying |
| 2 | Pain-led | The specific problem we eliminate |
| 3 | Category-defining | We're a new kind of thing |
| 4 | Segment-specific | For [role] at [company type] |
| 5 | Competitive | vs. the old way or doing nothing |
| 6 | Verbatim steal | Directly lifts a powerful customer phrase |
| 7 | Wildcard | Unexpected angle — makes the reader stop |

## Output Format (For Each Option)

```
### Option [N]: [Tone Label]
**Headline**: [Headline text]
**Subheadline**: [Subheadline text]
**Why this works**: [1–2 sentences on the strategic logic]
**Evidence**: [Specific quote or source document this draws from]
**Best for**: [A/B test scenario, audience segment, or page placement]
```

## After Writing

Write the 7 options to `outputs/homepage-headlines.md`.

Then give the user your personal top pick and 1-sentence rationale — which option best balances uniqueness, evidence strength, and ICP resonance.
