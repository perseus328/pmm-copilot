# Neubird AI — Competitive Profile

*Last updated: April 2026 · For internal use only*

**Key takeaway**: Resolve is an AI-for-production platform spanning multiple use cases. Neubird is an early AI SRE point tool — single-flow investigation, read-only by design, no continuous learning, and meaningful compliance gaps for regulated industries.

---

## Company Snapshot

**Neubird**
- Hawkeye launched December 2024 — ~16 months in market
- Falcon engine released April 2026
- ~30–50 person team (estimated from funding + LinkedIn signals); no Forward Deployed Engineers documented
- 14-day free self-service trial; also listed on AWS Marketplace
- Lacks named enterprise customer references in public materials
- SOC 2 Type II certified (Johanson Group LLP) — **no HIPAA, no PCI-DSS**
- SaaS + Private VPC deployment

**Resolve AI — the counter-position**
- Full-stack agent platform, in production at enterprise scale
- 130+ team; AI researchers from Google DeepMind and Meta SuperIntelligence; founders of OpenTelemetry; high-touch FDE support
- Named customers deployed at scale: Coinbase, DoorDash, Zscaler, Salesforce
- SOC 2 Type II · HIPAA · PCI-DSS · RBAC per team · AES-256 · full audit trails
- SaaS · Satellite (in-VPC) · data never leaves customer infrastructure

---

## Platform Gaps — What Neubird Can't Do

### 1. Single flow vs. multi-agent
*No parallel agents. No critique loop.*

Neubird runs a single coordinated investigation flow — fine-tuned Llama 3.3 + Claude reasoning models, guided by their RAEL telemetry reasoning language and LARK grammar files. Sophisticated architecture, but one sequential flow, not parallel agents.

**Resolve**: Autonomous incident investigations with a planner + specialized sub-agents + critique agent running in parallel. Multiplayer investigations. L3 RCA depth delivered to L1 responders. Auto-investigates alerts without operator prompting.

### 2. Read-only remediation
*Stops at the recommendation.*

Neubird is architecturally read-only — every connection is enforced read-only by design, so modification is technically impossible. Even with Falcon, actions are advisory. Actual execution requires Neubird Desktop CLI + an external coding agent (e.g., Claude Code via MCP). No native kubectl, rollback, config change, or PR execution.

**Resolve**: Executes PRs, kubectl commands, config changes, and rollbacks natively — with customer-defined human approval gates before any production change and a full audit trail.

### 3. No continuous learning
*Knowledge doesn't compound.*

No documented continuous learning mechanism exists in Neubird's production architecture. Their own documentation states "self-improving knowledge is an active research problem, not solved." Investigations do not compound into institutional knowledge for the next on-call engineer.

**Resolve**: Auto-builds a Knowledge Graph of infra, apps, teams, dependencies, and failure patterns. Self-updates after every investigation. Learning compounds across the enterprise.

### 4. Integration gap
*~20 connectors vs. 50+. Compliance gaps.*

Neubird documents ~20 named integrations: Datadog, Splunk, Prometheus, Grafana, New Relic, InfluxDB, Elasticsearch, PagerDuty, ServiceNow, Slack, GitHub, GitLab, Jira, AWS, Azure, GCP, IBM Cloud, VMware, OpenTelemetry.

**Resolve**: 50+ native integrations and MCP — observability + cloud + ITSM + source code + collaboration. Queries tools live with no data duplication. Plus HIPAA and PCI-DSS coverage that Neubird lacks — a hard disqualifier for regulated industries.

---

## Detailed Comparison

### Data access & integrations

**Resolve AI**
- Queries live into Datadog, Splunk, Grafana, Prometheus, AWS, Azure, GCP, K8s, GitHub, ServiceNow, Jira simultaneously
- Full-stack: observability + cloud + ITSM + source code + collaboration via 50+ native integrations and MCP
- No data duplication — queries tools in real time

**Neubird AI**
- ~20 named integrations (Datadog, Splunk, Prometheus, Grafana, New Relic, InfluxDB, Elasticsearch, PagerDuty, ServiceNow, Slack, GitHub, GitLab, Jira, AWS, Azure, GCP, IBM Cloud, VMware, OpenTelemetry)
- No write access — every connection architecturally enforced as read-only

*Sources: neubird.ai/blog/how-hawkeye-works-deep-dive-secure-genai-powered-it-operations · aws.amazon.com/blogs/apn/how-neubirds-hawkeye-transforms-it-operations-with-amazon-bedrock · neubirdai.github.io/hawkeye-mcp-docs*

---

### AI investigation depth

**Resolve AI**
- Multi-agent: planner + sub-agents + critique agent running in parallel
- Interactive — follow-ups, pivots, mid-stream context
- L3 RCA depth for L1 responders
- Auto-investigates alerts you care about
- Supports autonomous investigations AND collaborative multiplayer incident remediation

**Neubird AI**
- Single coordinated investigation flow — fine-tuned Llama 3.3 + Claude reasoning models, guided by Neubird's RAEL telemetry reasoning language and LARK grammar files
- Agent handoff via MCP — can pass diagnosed root cause to external coding agents (e.g., Claude Code) for implementation
- **Key architectural gap**: single sequential flow vs. Resolve's parallel multi-agent architecture

*Sources: help.neubird.ai (fine-tuning docs, RAEL/LARK reference) · neubird.ai/blog/how-hawkeye-works-deep-dive-secure-genai-powered-it-operations · aws.amazon.com/blogs/apn/how-neubirds-hawkeye-transforms-it-operations-with-amazon-bedrock*

---

### Remediation execution

**Resolve AI**
- Executes: PRs, kubectl commands, config changes, rollbacks
- Customer-defined human approval gates before any production change
- Full audit trail of every action taken

**Neubird AI**
- Architecturally read-only — every connection enforces read-only permissions by design; modification is technically impossible
- Recommendation engine only — provides step-by-step remediation guidance but does not execute natively
- External execution only — Neubird Desktop CLI + coding agent (e.g., Claude Code) required for any actual execution
- No native kubectl, rollback, config change, or PR execution

*Sources: neubird.ai/blog/how-hawkeye-works-deep-dive-secure-genai-powered-it-operations · help.neubird.ai/introduction/security-policy*

---

### Knowledge & continuous learning

**Resolve AI**
- Auto-builds a Knowledge Graph of infra, apps, teams, dependencies, failure patterns
- Self-updates after every investigation
- Cross-enterprise learning compounds over time

**Neubird AI**
- No cross-enterprise learning mechanism in production
- Neubird's own documentation states "self-improving knowledge is an active research problem, not solved"
- Investigations do not compound into institutional knowledge

*Sources: neubird.ai/blog/how-hawkeye-works-deep-dive-secure-genai-powered-it-operations · venturebeat.com (Falcon/FalconClaw launch, April 2026)*

---

### Time to value & maintenance

**Resolve AI**
- Days to first investigation
- Pre-built integrations, vendor-managed
- 130+ team, 70 eng/research; Forward Deployed Engineers for onboarding
- No prerequisite buildout — works with existing tools as-is

**Neubird AI**
- 14-day free self-service trial; also available on AWS Marketplace
- ~40 person team (estimated from funding/LinkedIn signals)
- No Forward Deployed Engineers documented

*Sources: businesswire.com (Free Trial launch, Dec 2025) · aws.amazon.com/marketplace/pp/prodview-gjxqnuba3boy2 · help.neubird.ai/introduction/security-policy*

---

### Security & deployment

**Resolve AI**
- SaaS, Satellite (in-VPC)
- SOC 2 Type II · HIPAA · PCI-DSS
- No customer data used for AI training
- RBAC per team · AES-256 at rest · TLS 1.2+ in transit · full audit trails

**Neubird AI**
- SOC 2 Type II certified only (audit by Johanson Group LLP)
- RBAC + SSO/SAML
- **No HIPAA. No PCI-DSS.** Neither certification publicly documented — disqualifying for regulated industries

*Sources: neubird.ai/blog/neubird-achieves-soc-2-compliance · help.neubird.ai/introduction/security-policy · aws.amazon.com/blogs/apn/how-neubirds-hawkeye-transforms-it-operations-with-amazon-bedrock*

---

## Evidence Notes

All Neubird claims sourced from public documentation, blog posts, press releases, and AWS partner materials as of April 9, 2026.
