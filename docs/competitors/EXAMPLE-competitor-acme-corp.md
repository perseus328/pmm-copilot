# Competitor Profile — Competitor A (Data Monitoring Co.)
**Last updated**: February 2024
**Sources**: Sales call notes, win/loss interviews, G2 reviews, public website

---

## Overview

Competitor A is a data observability platform focused on rule-based monitoring and data quality testing. Founded 2019, Series C ($85M raised), ~200 employees. Positioned as "the data reliability platform."

**Where they show up**: We encounter them in 40-50% of competitive deals. Most common scenario: prospect evaluated them first, ran into the rule-writing limitation, then found us.

---

## What They Do Well

- **Large connector library**: 300+ pre-built connectors vs. our 150. This is a real weakness for us in deals where connector breadth is the primary evaluation criterion.
- **dbt integration**: Deep, native dbt integration is genuinely better than ours. Prospects with heavy dbt usage often prefer them.
- **G2 reviews**: Excellent G2 ratings (4.6/5, 400+ reviews). Strong social proof, especially for mid-market.
- **Sales team**: Well-resourced, fast response times, good at running POCs. We lose on deal execution speed sometimes.

---

## What Customers Say About Their Weaknesses

> "Their alerting is entirely rule-based. You have to know what to monitor in advance. We don't always know what we don't know." — Source: EXAMPLE-sales-call-2024-03.md, VP of Operations at DataFlow Inc

> "The thing that [Competitor A] could never do was tell me that something was *probably about to break* — they could only tell me it had already broken. That's the fundamental difference." — Source: EXAMPLE-customer-interview-jane-smith.md, Head of Analytics at RetailNow

> "We set up 200+ monitors in [Competitor A] and still missed the incident that caused us to switch. The problem is that monitoring only catches what you explicitly test for." — Source: Customer win/loss call, March 2024 (unattributed)

---

## Win/Loss Patterns

### We Win When:
- Prospect has complex, heterogeneous data sources (not just standard SaaS connectors)
- Prospect has experienced an incident that rules-based monitoring didn't catch
- Evaluation is led by Ops/Analytics rather than Engineering (our buyers vs. their buyers)
- Prospect is scaling fast and doesn't have bandwidth to write and maintain hundreds of monitors

### They Win When:
- Prospect's primary need is connector coverage (they win on breadth)
- Prospect is deeply invested in dbt (their dbt integration is better)
- Deal moves fast and they out-execute us on POC speed
- Prospect values brand/logo recognition (they have more enterprise logos)

---

## Pricing Signals

Based on competitive intel from prospects: Competitor A prices at roughly 15-20% less than us at the mid-market level. At enterprise, pricing is comparable. They are NOT the budget option — do not let prospects position them as cheaper without checking their actual quote.

---

## Messaging to Avoid When Competing Against Them

- Do NOT compete on connector count — they have more
- Do NOT compete on G2 reviews — they have more reviews and similar rating
- Do NOT compete on dbt integration depth

---

## Trap Questions to Use

- "When you set up monitors in their platform, who writes the detection rules?"
- "What happens when your data fails in a way you didn't anticipate and never wrote a rule for?"
- "How much time does your team spend maintaining your monitoring configuration as your data evolves?"

---

## PMM Notes

- Their core positioning is "data reliability" — we can own "data awareness" or "data intelligence" as a distinct space
- Their Achilles heel is the rule-writing burden — every rep should know this cold
- When prospects say "we're evaluating [Competitor A]", ask: "have they shown you what happens with an anomaly type you've never seen before?"
