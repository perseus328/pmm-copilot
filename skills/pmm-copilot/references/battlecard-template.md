# Battlecard Template

## Purpose

A battlecard is a 1-page reference document for sales reps to use in real-time competitive conversations. It should be scannable in 30 seconds and immediately actionable. It is NOT a competitive analysis document — it's a conversation tool.

**Guiding principle**: Only include things a rep can actually say in a live sales call. If it requires a paragraph to explain, it doesn't belong on a battlecard.

---

## Structure

### Header
```
[Our Product] vs. [Competitor]
Updated: [Date] | Owner: [PMM Name]
One-liner: "We win when [scenario]. They win when [scenario]."
```

The one-liner is the most important line on the card. Reps should memorize it.

---

### Section 1: Handle the Objection

When a prospect brings up this competitor, these are the objections reps will hear. Each needs a response that:
- Acknowledges the concern (don't be defensive)
- Pivots to a genuine differentiator
- Is sayable in one breath

| When They Say | You Say |
|--------------|---------|
| "[Competitor] has been around longer" | "You're right, they have — and their architecture reflects that. We were built from the ground up for [modern scenario]..." |
| "We're already evaluating [Competitor]" | "Great — while you're doing that, I'd love to show you how we handle [our strength area]. What does [scenario] look like in their demo?" |
| "Your price is higher" | "Our customers find the ROI is [specific outcome]. [Customer name/type] was able to [specific result] within [timeframe]." |

**Source**: Pull these from call notes where reps have documented actual objections heard.

---

### Section 2: Where We Win

3 specific scenarios where we beat them. Each entry needs:
- **Scenario**: The situation that triggers a win for us
- **Why we win**: The specific capability that matters in this scenario
- **Proof point**: Customer quote or case study reference (with source)

Example:
> **Scenario**: Prospect has complex, heterogeneous data sources (not just standard SaaS connectors)
> **Why we win**: Our schema-free ingestion handles arbitrary data shapes without pre-configuration
> **Proof**: "We had 14 custom data sources that [Competitor] said would require professional services. We had them running in 3 days." — Source: EXAMPLE-customer-interview-jane-smith.md

---

### Section 3: Their Real Weaknesses

3 honest limitations of the competitor — things customers have actually complained about. No speculation.

Format:
> "[Competitor] struggles with [X]. Evidence: '[customer quote]'" — Source: [filename]

**Critical rule**: If you don't have customer evidence for a weakness, don't include it. Made-up weaknesses destroy rep credibility when prospects have a different experience.

---

### Section 4: Trap Questions

2–3 discovery questions that expose areas where we win when the prospect answers honestly. These are designed to create "aha" moments, not to trick anyone.

Format: "How do you currently handle [our strength area] when [trigger scenario]?"

Examples:
- "How do you find out today when a data pipeline has failed and downstream teams are already affected?"
- "What happens when you need to add a new data source that wasn't in your original setup?"
- "Who gets the call when the CEO asks why a dashboard number looks wrong?"

---

### Section 5: Landmines to Avoid

1–2 topics to redirect away from — areas where we're genuinely weaker. Be honest with your sales team.

Format:
> **Avoid**: [Topic]
> **Why**: [Honest assessment]
> **If it comes up**: [How to redirect without lying]

Example:
> **Avoid**: Deep comparison of pre-built connector count
> **Why**: [Competitor] has 300+ connectors vs. our 150
> **If it comes up**: "Connector count matters for simple pipelines. For complex environments like yours, the bottleneck is usually monitoring and alerting, not ingestion — let me show you that."

---

## Formatting Notes for the Generated Output

- Keep each section to 3 items maximum — more than that and reps won't remember any of it
- Use bold for the key phrase in every entry — reps scan for bold text under pressure
- Add the generation date and a "review by" date (+90 days) — stale battlecards are dangerous
- The whole card should fit on one printed page (or one screen without scrolling)
