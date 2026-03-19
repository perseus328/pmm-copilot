---
description: Generate a PMM deliverable using parallel sub-agent analysis. Run /ingest first.
allowed-tools: Read, Write, Glob
argument-hint: "positioning | headlines | battlecard | launch-brief | all"
---

# Generate PMM Deliverable

Generate the requested PMM deliverable: `$ARGUMENTS`

## Pre-Flight Check

Before doing anything else:
1. Check if `outputs/research-synthesis.md` exists. If it does NOT exist, stop immediately and tell the user: "Run `/ingest` first to build the research synthesis. The generate command requires that file to produce evidence-backed output."
2. Read `outputs/research-synthesis.md` and `CLAUDE.md` to load full context.

---

## Routing by Output Type

### `positioning`

Launch **3 sub-agents IN PARALLEL** to analyze different dimensions simultaneously:

**Sub-agent 1 — voice-of-customer**:
"Read docs/calls/ and docs/interviews/ along with outputs/research-synthesis.md. Extract the top 5 recurring customer language themes with verbatim quotes. Identify the top 3 jobs-to-be-done. Return structured findings with source citations."

**Sub-agent 2 — competitor-analyst**:
"Read docs/competitors/ and competitive mentions in outputs/research-synthesis.md. Map all competitive alternatives. For each, identify: why customers consider them, where we win, where they win, and verbatim customer quotes about them. Return structured findings."

**Sub-agent 3 — message-gap-detector**:
"Read docs/positioning/ and outputs/research-synthesis.md. Compare what customers say they care about vs. what our current positioning emphasizes. List the top 3 gaps with specific evidence. Return structured findings."

Wait for all 3 agents to complete, then synthesize their outputs into a positioning statement following the April Dunford framework from CLAUDE.md. Tag every claim with its evidence source.

Write result to `outputs/positioning-statement.md`.

---

### `headlines`

Run `/headlines` logic directly (see `.claude/commands/headlines.md` for full instructions). Write to `outputs/homepage-headlines.md`.

---

### `battlecard`

Run `/battlecard` logic directly (see `.claude/commands/battlecard.md` for full instructions). Write to `outputs/battlecard.md`.

---

### `launch-brief`

Read the template at `skills/pmm-copilot/references/launch-brief-template.md`. Fill in every section using all available research from `outputs/research-synthesis.md` and `docs/`. Tag every claim with evidence. Mark any section with insufficient evidence as [NEEDS EVIDENCE — describe what research would fill this gap].

Write to `outputs/launch-brief.md`.

---

### `all`

Run all four sequences above in the most efficient order:
1. First: `positioning` (requires parallel agents — do this first while context is freshest)
2. Then: `headlines`, `battlecard`, `launch-brief` (can use positioning output as additional input)

After all four complete, write `outputs/session-summary.md` listing every file generated, its word count, and a 1-line description of what it contains.

---

### Unrecognized argument

Tell the user: "Available options: `positioning`, `headlines`, `battlecard`, `launch-brief`, `all`"
Show a brief description of each option.
