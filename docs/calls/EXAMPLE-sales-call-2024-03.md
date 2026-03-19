# Sales Call Notes — Prospect: DataFlow Inc
**Date**: March 14, 2024
**Rep**: Sarah Chen
**Prospect Role**: VP of Operations
**Company**: DataFlow Inc (Series B, 180 employees, logistics SaaS)
**Stage**: Discovery → moved to technical evaluation

---

## Context

DataFlow processes 50,000+ shipments/day. Currently running a homegrown stack: Fivetran for ingestion + dbt for transforms + manual SQL alerting. Came inbound after seeing our pricing page. Prior to this call had not done a formal data observability evaluation.

---

## Key Moments

**On current pain:**
> "The biggest problem isn't the data pipeline itself — it's that by the time I know something's broken, it's already affected three downstream teams. We have a six-hour lag between incident and awareness."

> "We've had two near-misses this quarter where finance reported wrong numbers to the board because their dashboard was pulling from stale data. That's a career risk for me personally."

**On what they actually want:**
> "I don't need a prettier dashboard. I need to stop being surprised. I want to know before my CEO does that something is wrong."

**On current alerting:**
> "We have some SQL-based monitors set up but they only catch things we anticipated. The stuff that kills us is the thing nobody thought to write a rule for."

**On evaluating competitors:**
> "We looked at [Competitor A] — their alerting is entirely rule-based. You have to know what to monitor in advance. We don't always know what we don't know."

**On budget/pricing:**
> "If this saves me one board-level embarrassment a year, it pays for itself. The cost isn't my concern. My concern is whether it actually works on our data."

---

## Objections Raised

1. "Our engineering team is skeptical of adding another tool to the stack" — addressed by noting API-first architecture and no required agents
2. "How do we know the anomaly detection will work on our data specifically?" — agreed to run a proof-of-concept on their actual pipeline

---

## Competitive Signals

- Evaluated: Competitor A (ruled out — rule-based only)
- Still using: Fivetran (happy with ingestion, not replacing it)
- True alternative: "We'd probably just hire another data engineer to babysit the pipelines"

---

## Outcome

Moved to technical evaluation. Wants to see the anomaly detection running on their actual Fivetran + dbt data within 2 weeks.

---

## PMM Notes

- **Headline candidate**: "Stop being surprised by data failures"
- **Headline candidate**: "Know before your CEO does"
- **Buyer framing**: VP of Ops, not VP of Data — ops accountability for data quality is the real pain
- **Key differentiator signal**: ML-based vs. rule-based alerting was the deciding factor vs. Competitor A
- **Stealth competitor**: Hiring a data engineer (headcount, not software)
- **Board-level risk framing**: High signal — this is a career-risk purchase, not a tooling purchase
