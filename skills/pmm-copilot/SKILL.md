---
name: pmm-copilot
description: >
  This skill should be used when the user discusses any of the following: "positioning",
  "messaging", "battlecard", "launch brief", "homepage headline", "customer research",
  "voice of customer", "competitive differentiation", "ICP", "value proposition",
  "message-market fit", "PMM", "product marketing", "go-to-market", "GTM", "launch",
  "sales enablement", or creating marketing copy based on customer evidence.

  Provides PMM methodology, output quality standards, and evidence discipline for all
  messaging work — auto-activates so quality standards apply even in casual conversation.
version: 0.1.0
---

# PMM Messaging Copilot Skill

This skill provides core product marketing methodology and quality standards for all messaging work in this project.

## Quality Tests (Apply to Every Output)

Before finalizing any PMM deliverable, run these four tests:

**The Uniqueness Test**
Could a competitor say the same thing? If yes, it's a category claim, not a positioning claim.
Action: Flag with [NOT DIFFERENTIATED] and push for what's genuinely unique.

**The Evidence Test**
Every claim needs a customer quote, data point, or named source.
Action: Flag unsupported claims with [NEEDS EVIDENCE — describe what would fill this gap].

**The "So What?" Test**
For every feature or capability mentioned, state what it enables for the buyer.
Wrong: "Real-time data sync" → Right: "Real-time data sync so ops teams catch errors before they propagate downstream"

**The Language Test**
Does the output use words the ICP actually uses, or internal company jargon?
Reference: Check `outputs/research-synthesis.md` → "Language to Steal" section.

## Positioning Framework (April Dunford)

When generating a positioning statement, structure it as:

```
For [specific buyer persona]
Who [specific pain or job to be done, in their words]
[Product Name] is a [market category]
That [primary value — stated as an outcome]
Unlike [primary competitive alternative]
We [specific differentiator the alternative genuinely cannot match]
```

The market category choice determines everything else — if it's wrong, no amount of messaging fixes it.

## When to Use Parallel Sub-Agents

**Work directly** (no sub-agents needed) when:
- Answering a single question about messaging
- Editing one section of an existing deliverable
- Fewer than 3 source documents to analyze

**Launch sub-agents in parallel** when:
- Generating a positioning statement from scratch
- Running a full message gaps critique
- The task requires both "what customers say" AND "what we currently say" analysis
- More than 3 source documents need synthesis

Agents to use: `voice-of-customer`, `competitor-analyst`, `message-gap-detector`

## Output File Standards

Every file written to `outputs/` should include:
- Generation date at the top
- Source documents referenced
- Evidence confidence markers: [HIGH — 3+ sources] / [MEDIUM — 2 sources] / [LOW — 1 source / inferred]

## Reference Materials

Detailed templates and frameworks are in `skills/pmm-copilot/references/`:
- `positioning-framework.md` — Full April Dunford framework with worked examples
- `battlecard-template.md` — Sales battlecard structure and copy guidance
- `launch-brief-template.md` — Launch brief with all required sections

Load these on demand when generating the corresponding deliverable type.
