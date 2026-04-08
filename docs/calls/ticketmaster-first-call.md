# Resolve AI x Ticketmaster — Call Transcript

---

## Participants

- Remington Gack (Resolve AI)
- Jason Kabalker (Resolve AI)
- Amal (Resolve AI)
- Yevhen Zavhorodnii (Principal SRE, Ticketmaster)

---

## Introductions

- Jason Kabalker: Account Executive at Resolve, working with Ticketmaster stakeholders
- Amal: Leads service team, supports evaluations, integrations, and onboarding
- Yevhen Zavhorodnii: Principal SRE in Central SRE Consultants team at Ticketmaster

---

## Ticketmaster SRE Operating Model

- Central SRE team acts as **internal consultants**
- Engagements:
  - Typically **6–12 months**
  - Focus on:
    - Reliability
    - Availability
    - SRE culture
    - SLO adoption
- Goal:
  - Leave teams operating independently with improved practices

---

## Key Challenges

### 1. Noisy Alerts

- Many teams experience high alert volume
- Fully analyzing alerts would take **an entire workday**
- Leads to:
  - Alert fatigue
  - Ignored alerts unless critical

---

### 2. Major Incident-Driven Development

- Some teams operate reactively:
  - Only respond to major incidents
- Downsides:
  - Unsustainable “hero culture”
  - Constant firefighting
- Tracking was stopped due to **blameless culture concerns**

---

### 3. Knowledge Bottlenecks

- “Resilience Analysis” team:
  - Acts as incident coordinators
  - Serves as a **human knowledge base**
- Issues:
  - Heavy reliance on individuals
  - Not scalable
  - Desire for automation or augmentation

---

### 4. Fragmented Tooling

- Stack includes:
  - Splunk (Enterprise + Observability)
  - Kibana
  - Grafana
  - AWS / Kubernetes
  - PagerDuty
  - FireHydrant
  - GitHub
- Reality:
  - Teams have autonomy → “zoo of systems”
  - Platform team provides guidance, not enforcement

---

### 5. Cold Start Problem

- On-call engineers:
  - Often don’t know where to begin
  - Face multiple simultaneous symptoms
- Results in:
  - Slow MTTR
  - Escalation to multiple teams

---

## Resolve AI Overview

### Core Idea

- AI operates across:
  - Observability (logs, metrics, traces)
  - Infrastructure (Kubernetes, cloud)
  - Code (GitHub)
- Correlates signals to identify root cause

---

### Key Capabilities

#### Multi-Agent System
- Planner + sub-agents + critique agent
- Executes investigations in parallel

#### Cross-System Investigation
- Works across multiple tools simultaneously
- Eliminates need for manual navigation

#### Slack Integration
- Native workflows:
  - Auto-investigation summaries
  - Follow-up questions
  - Incident channel participation

#### Extendable Integrations
- Supports:
  - Native integrations
  - MCP (Model Context Protocol)
  - Custom APIs
- Handles edge cases (e.g., Databricks)

#### Context Graph
- Builds understanding of:
  - Kubernetes clusters
  - Services
  - Deployments
  - Dependencies
- Maintains real-time system map

---

### Action Capabilities

- Suggests:
  - `kubectl` commands
  - Configuration changes
- Can generate:
  - GitHub PRs
- Current model:
  - Human-in-the-loop (no autonomous execution)

---

## Workflow Example

1. Alert is triggered (e.g., from Splunk, Grafana, CloudWatch)
2. Resolve:
   - Starts investigation automatically
   - Queries logs, metrics, infra, code
3. Produces:
   - Findings
   - Hypothesis
   - Supporting evidence (linked to sources)
4. Output delivered in:
   - Slack
   - UI (optional)

---

## Slack-Based Interaction Modes

1. **Auto Investigation**
   - Resolve posts findings in Slack

2. **Interactive Debugging**
   - Ask follow-up questions
   - Example:
     - “Any recent deployments?”
     - “Check infra health”

3. **Incident Channel Participation**
   - Resolve joins incident channels
   - Provides real-time context and analysis

4. **Proactive Health Checks**
   - Trigger checks without alerts
   - Example:
     - Post-deploy validation

---

## User Feedback & Vision

### Desired Future State

- AI assists in:
  - Identifying responsible teams
  - Suggesting incident participants
- Real-time collaboration with AI
- Ability to:
  - Test fixes quickly (e.g., kubectl)
  - Validate hypotheses before committing changes

---

## Limitations

- No autonomous execution of infrastructure commands
- Requires human validation for changes
- Knowledge must be:
  - Integrated (via tools)
  - Or explicitly provided (runbooks)

---

## Next Steps

1. Wait for stakeholder (Nicolo) availability
2. Internal discussion within Ticketmaster
3. Identify pilot team
4. Run Proof of Concept (POC):
   - Central SRE + service team
5. Follow-up check-in (~2 weeks)

---

## Key Takeaways

- Ticketmaster challenges:
  - Alert fatigue
  - Knowledge bottlenecks
  - Fragmented tooling
- Resolve AI aligns with:
  - Cross-stack investigation needs
  - Faster root cause analysis
  - Reducing reliance on human expertise
- Next logical step: **POC with a real service team**