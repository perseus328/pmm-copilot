---
description: Generate a weekly "what changed" enablement pack from current PMM outputs
allowed-tools: Read, Write, Glob
argument-hint: "[optional date range or week label, e.g. 2026-W14]"
---

# Generate Weekly Enablement Update

Create a concise weekly "what changed" summary **for sales reps** (AEs, SDRs, SEs) from the latest PMM outputs. This is **field enablement**, not an internal PMM audit.

## Pre-Flight

Before analysis:
1. Check if `outputs/research-synthesis.md` exists. If not, stop and tell the user to run `/ingest` first.
2. Read these files if they exist:
   - `outputs/research-synthesis.md` (required)
   - `outputs/positioning-statement.md`
   - `outputs/message-gaps-critique.md`
   - `outputs/homepage-headlines.md`
   - `outputs/session-summary.md`
   - all `outputs/battlecard*.md`
3. Also read current baseline docs for context:
   - `docs/positioning/` (all `.md`)
   - `docs/competitors/` (all `.md`)
   - a sample of `docs/calls/` and `docs/interviews/` for verbatim grounding

If only `research-synthesis.md` exists, still generate the pack using available evidence and mark missing sections with `[NEEDS EVIDENCE]`.

## Tone & audience (required)

- **Write for reps on Monday morning:** practical, confident, and usable in live calls. Short sentences. No essay tone.
- **Do not** frame updates as "our positioning is weak," "contradicts our positioning," "internal messaging is wrong," or anything that sounds like the company narrative is failing. Reframe as **what buyers are saying**, **what to emphasize this week**, and **how to win the conversation**.
- **Do not** blame or shame reps. Avoid: "reps failed to…," "vague answers from the field," "you're not doing X." Use neutral or buyer-centric language: *"Buyers often ask…"*, *"A crisp answer that lands is…"*, *"Try leading with…"*
- **Internal critique** (gaps vs. official positioning, harsh claim audits) belongs in `outputs/message-gaps-critique.md` and similar — **do not copy that tone into this weekly pack.** If you reference critique outputs, translate them into **additive, forward-looking talk tracks** only.
- **Do not** use tables or sections that read like a scorecard against "our positioning." No "contradicted by data," "retire immediately," or similar.

## What to Extract

Build a delta-first summary focused on **behavior change for reps**:
- New or materially stronger **buyer** pain points (with quotes)
- New competitive signals and how to **position us** in those moments
- **What to emphasize** in discovery and demos this week (additive framing — not "old wrong / new right")
- Proof points and soundbites reps can use
- Product/category language that lands better with buyers vs. terms that create confusion (about **customer-facing** words, not internal doc quality)

Only include changes supported by evidence. If evidence is thin, flag with `[NEEDS EVIDENCE]`.

## Output File

Write to:
- `outputs/weekly-what-changed-$ARGUMENTS.md` if an argument is provided
- `outputs/weekly-what-changed.md` if no argument is provided

Use this format (no Executive Delta section):

```
# What Changed This Week
Date: [today]
Period: [$ARGUMENTS or "Current snapshot"]
Audience: Sales reps (AE / SDR / SE)
Sources reviewed: [list]

## Customer Signal Shifts
### New or stronger pains
- [Pain] — [frequency/signal] — "[best quote]" — Source: [file]

### Desired outcomes gaining importance
- [Outcome] — "[quote]" — Source: [file]

## Competitive Changes
- [Competitor/alternative] — [what we're hearing] — [how to position us / talk track] — Source: [file]

## What to emphasize this week
For each item, use **buyer-forward** language. Prefer:
- **Lead with:** … (outcome or question)
- **Why it matters:** … (buyer context)
- **Proof:** "[quote or stat]" — Source: [file]

Avoid subheadings like "Old framing" / "New framing" that imply internal messaging was wrong. Use **Prioritize**, **Add to discovery**, or **Stronger angle in market** instead.

## Rep-ready actions this week
1. Discovery question: "[question]"
2. Objection or competitive response: "[response]"
3. Trap / qualification question: "[question]"
4. Proof point to lead with: "[soundbite]"
5. On calls, prefer saying ___ over ___ (customer-facing language only — e.g. category terms that confuse buyers)

## Proof points & language to use
- Bullet list of the strongest **customer-backed** lines reps can repeat
- Optional: **Terms that create friction on calls** — describe what **buyers** react to, not what is "wrong" with internal docs

## NotebookLM Asset Prompts
- Audio briefing prompt: [prompt text — upbeat, practical, rep as hero of the story]
- Quiz prompt: [prompt text]
- Role-play prompt: [prompt text]
```

## Final User Report

After writing, provide:
1. A 3–5 bullet summary of what reps should **do** this week (action-only, confident tone)
2. One line: the **strongest buyer signal** to lean into
3. A suggested next command only if it helps the field (`/battlecard [competitor]`, `/headlines`, etc.)
