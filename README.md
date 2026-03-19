# PMM Messaging Copilot

A Claude Code project that turns raw customer research into polished PMM deliverables — and demonstrates every major Claude Code primitive along the way.

## What It Does

Drop your research files into `docs/` and run slash commands to generate:
- **Positioning statement** — April Dunford framework, evidence-backed
- **Homepage headlines** — 7 options with tone variety and customer language
- **1-page battlecard** — objection handlers, trap questions, landmines to avoid
- **Launch brief** — full cross-functional alignment doc
- **Message gaps critique** — 5-dimension scoring of your current messaging vs. customer reality

## Claude Code Primitives Demonstrated

| Primitive | File(s) | Purpose |
|-----------|---------|---------|
| **CLAUDE.md** | `CLAUDE.md` | Project memory: product context, ICP, methodology, quality tests |
| **Slash commands** | `.claude/commands/` | Repeatable workflow entry points (`/ingest`, `/generate`, etc.) |
| **Sub-agents** | `agents/` | Parallel analysis from 3 specialized lenses simultaneously |
| **Skill** | `skills/pmm-copilot/` | Auto-activating PMM methodology + templates (loads on context match) |
| **Hooks** | `.claude/settings.json` | SessionStart setup check, PostToolUse evidence guard, Stop gate |

## Quick Start

### 1. Set your product context
Edit `CLAUDE.md` — fill in your product name, stage, and ICP.

### 2. Add your research
Drop your files into the appropriate `docs/` subfolder:
```
docs/
├── calls/          ← sales call notes or transcripts
├── interviews/     ← customer interview notes
├── positioning/    ← current positioning or messaging docs
└── competitors/    ← competitor profiles, win/loss notes
```
Files prefixed `EXAMPLE-` are sample files showing the expected format. Replace them with your own.

### 3. Run the workflow

```
/ingest                    # Step 1: synthesize all research → outputs/research-synthesis.md
/critique                  # Optional: score your current messaging gaps first
/generate positioning      # Generate positioning statement (launches 3 parallel agents)
/battlecard acme-corp      # Generate a competitor-specific battlecard
/headlines                 # Generate 7 homepage headline options
/generate launch-brief     # Generate a full launch brief
/generate all              # Run all four deliverables in one go
```

All outputs land in `outputs/`.

## Project Structure

```
pmm-copilot/
├── CLAUDE.md                          # Product context + PMM methodology
├── .claude/
│   ├── settings.json                  # Hooks (SessionStart, PostToolUse, Stop)
│   └── commands/                      # Slash commands
│       ├── ingest.md                  # /ingest
│       ├── generate.md                # /generate [type]
│       ├── battlecard.md              # /battlecard [competitor]
│       ├── headlines.md               # /headlines
│       └── critique.md                # /critique
├── agents/                            # Sub-agents (run in parallel)
│   ├── voice-of-customer.md           # Extracts verbatims and language themes
│   ├── competitor-analyst.md          # Synthesizes competitive intelligence
│   └── message-gap-detector.md       # Finds gaps between messaging and research
├── skills/pmm-copilot/
│   ├── SKILL.md                       # Auto-activating PMM quality standards
│   └── references/                    # Templates loaded on demand
│       ├── positioning-framework.md   # April Dunford framework
│       ├── battlecard-template.md     # Sales battlecard structure
│       └── launch-brief-template.md   # Launch brief all sections
├── docs/                              # Your research goes here
│   ├── calls/
│   ├── interviews/
│   ├── positioning/
│   └── competitors/
└── outputs/                           # Generated deliverables land here
```

## How the Primitives Work Together

```
User runs /ingest
  └─ Claude reads all docs/ files
  └─ Writes outputs/research-synthesis.md

User runs /generate positioning
  └─ /generate command checks for research-synthesis.md (guard rail)
  └─ Spawns 3 sub-agents IN PARALLEL:
       ├─ voice-of-customer    (green)  → customer language themes
       ├─ competitor-analyst   (cyan)   → competitive landscape
       └─ message-gap-detector (magenta)→ current messaging gaps
  └─ Synthesizes agent outputs → outputs/positioning-statement.md
  └─ PostToolUse hook fires → checks for unsupported claims
  └─ Stop hook fires → blocks if citations are missing

Meanwhile, pmm-copilot SKILL auto-activates on any PMM language
  └─ Applies Uniqueness Test, Evidence Test, "So What?" Test to all output
```
