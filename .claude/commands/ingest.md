---
description: Read and index all research documents in docs/ — run this first before any generate commands
allowed-tools: Read, Glob, Write
argument-hint: "[optional subfolder: calls | interviews | positioning | competitors]"
---

# Ingest Research Documents

Perform a full ingestion of PMM research materials from the `docs/` folder (or `docs/$ARGUMENTS/` if a subfolder was specified).

## Step 1: Find Documents

Use Glob to find all `.md` files in the target folder. If no documents are found:
- Show the user the expected folder structure
- Explain which file types belong in each subfolder
- Stop here and tell them to add their research files before re-running

## Step 2: Read and Extract

Read every file found. For each document, extract:

- **Document type** (call note / customer interview / positioning doc / competitor profile)
- **Key customer quotes** — verbatim language worth preserving (exact wording, not paraphrase)
- **Pain points** — problems the customer named explicitly
- **Desired outcomes** — what success looks like in their words
- **Competitive mentions** — any competitor names, alternatives, or "what we used before" references
- **Objections or concerns** raised
- **Buyer role and company context** — seniority, company type, company size if available

## Step 3: Write Research Synthesis

Write a synthesis file to `outputs/research-synthesis.md` with this structure:

```
# Research Synthesis
Generated: [today's date]
Documents ingested: [count and list of filenames]

## Customer Voice Themes
[Top 5–7 recurring themes, each with 2+ supporting verbatim quotes and their source files]

## Pain Point Inventory
[Ranked by frequency. Format: Pain → # of sources → best verbatim quote]

## Jobs To Be Done
[What are customers actually trying to accomplish? Not the product — the job]

## Competitive Landscape Signals
[Competitors and alternatives mentioned, with customer context for each]

## Messaging Gaps (Preliminary)
[What do customers care about that seems absent from our current positioning docs?]

## Raw Evidence Bank
[All notable verbatim quotes, tagged: "quote" — Source: filename, role/company]
```

## Step 4: Report to User

After writing the synthesis file, give the user a 3–5 bullet summary:
- How many documents were ingested
- The top 2–3 customer themes found
- Any notable gaps spotted
- Which command to run next (suggest `/critique` to score current messaging, or `/generate positioning` to start building)

If documents were skipped or had insufficient content, flag them by name.
