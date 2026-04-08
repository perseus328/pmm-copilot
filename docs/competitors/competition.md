## Resolve AI vs. Alternatives

### Data Access & Integrations

**Resolve AI**
- Queries live into Datadog, Splunk, Grafana, Prometheus, AWS, Azure, GCP, K8s, GitHub, ServiceNow, Jira simultaneously  
- Full-stack: observability + cloud + ITSM + source code + collaboration via 50+ native integrations and MCP  
- No data duplication: queries tools in real time  

**The Alternatives**
- **Observability platforms**: Locked to their own data  
  - Datadog Bits AI only sees Datadog  
  - Dynatrace Davis only sees Dynatrace  
  - Cannot investigate cross-tool — the #1 gap in enterprise incident response  
- **Incident platforms**: Alert stream only  
  - PagerDuty has no access to logs, metrics, or infrastructure  
  - ServiceNow depends on CMDBs that go stale within weeks  
- **AI SRE startups**: Limited integration breadth vs. 50+ at Resolve  
- **Labs / DIY**:  
  - Every connector is custom-built  
  - Integrations are brittle and require constant maintenance  

---

### AI Investigation Depth

**Resolve AI**
- Multi-agent: planner + sub-agents + critique agent in parallel  
- Interactive: follow-ups, pivots, mid-stream context  
- Brings L3 RCA to L1 responders  
- Auto-investigation of alerts  

**The Alternatives**
- **Observability platforms**:  
  - AI is a bolt-on, not core  
  - Summarizes alerts but does not investigate root cause  
  - Cannot pivot mid-investigation or reason across layers  
- **Incident platforms**:  
  - Static playbooks for known failures only  
  - Novel incidents require humans from scratch  
- **AI SRE startups**:  
  - Single-shot investigations  
  - No cross-stack reasoning  
- **Labs / DIY**:  
  - LLMs suggest queries; humans execute  
  - Sequential and manual  

---

### Remediation Execution

**Resolve AI**
- Executes: PRs, kubectl commands, config changes, rollbacks  
- Human approval gates before production changes  
- Full audit trail  

**The Alternatives**
- **Observability platforms**: Limited to platform-specific actions  
- **Incident platforms**: Ticketing and escalation only  
- **AI SRE startups**: Mostly read-only; some generate PRs but stop at recommendations  
- **Labs / DIY**: Fully manual with no guardrails or audit trail  

---

### Knowledge & Continuous Learning

**Resolve AI**
- Auto-builds Knowledge Graph: infrastructure, apps, teams, dependencies, failure patterns  
- Self-updates after every investigation  
- Cross-enterprise learning compounds  

**The Alternatives**
- **Observability platforms**: No cross-incident learning; each alert is isolated  
- **Incident platforms**: Static CMDB + manual runbooks; quickly stale  
- **AI SRE startups**: Continuous learning not production-ready  
- **Labs / DIY**: No memory; every incident starts from zero  

---

### Time to Value & Maintenance

**Resolve AI**
- Days to first investigation  
- Pre-built integrations, vendor-managed  
- 130+ team, 70 eng/research, Forward Deployed Engineers  
- No prerequisite buildout  

**The Alternatives**
- **Observability platforms**: Fast only if fully consolidated; high per-use cost  
- **Incident platforms**:  
  - CMDB buildout: 3–6 months  
  - Full AI autonomy: 18+ months  
- **AI SRE startups**: Weeks to months; smaller teams  
- **Labs / DIY**:  
  - 10–15 engineers, 18–24 months  
  - Fragile and high maintenance  

---

### Security & Deployment

**Resolve AI**
- SaaS, satellite (in-VPC), or air-gapped  
- Data remains within customer infrastructure  
- SOC 2 Type II, HIPAA, PCI-DSS  
- RBAC per team, AES-256 at rest, TLS 1.2+ in transit  
- Full audit trails  

**The Alternatives**
- **Observability platforms**: SaaS-only AI features; data residency concerns  
- **Incident platforms**: On-prem workflow but SaaS AI layer  
- **AI SRE startups**: Mostly SaaS; limited compliance  
- **Labs / DIY**: Security, compliance, and audit fully owned internally  

---

## Observability Platforms  
*(Datadog Bits AI, Dynatrace Davis, Splunk, Grafana)*

Observability platforms are adding AI, but these are bolt-on features—not purpose-built investigation systems.

- AI is restricted to platform-specific data  
- Enterprise environments use 5–10+ tools → no unified visibility  
- Cannot investigate cross-tool incidents  

**Examples**
- **Datadog Bits AI**  
  - SaaS-only  
  - Limited to Datadog telemetry  
  - Per-investigation pricing scales unpredictably  
- **Dynatrace Davis**  
  - Agentic remediation still in preview  
  - Limited to Dynatrace-ingested data  
- **Splunk / Grafana**  
  - No autonomous investigation  
  - Fully human-driven workflows  

**Why Resolve AI**
- Purpose-built for production investigation  
- Multi-agent reasoning layer across the full stack  
- Works across existing tools without replacing them  
- Enterprise-grade deployment and security  

---

## Incident Platforms  
*(ServiceNow, PagerDuty)*

Incident platforms manage alerts—they do not investigate.

- **PagerDuty**: Routing and alert context only; no root cause investigation  
- **ServiceNow**:  
  - Depends on stale CMDBs  
  - No autonomous investigation  

**Why Resolve AI**
- Investigates root cause, not just alerts  
- Delivers remediation before human intervention  
- Proven results:  
  - Coinbase: 72% faster investigations  
  - DoorDash: 87% faster  
  - Zscaler: 30% fewer engineers per incident  

---

## AI SRE Startups  
*(Traversal, Deductive, Cleric)*

Emerging category with gaps in scale, maturity, and enterprise readiness.

- **Funding gap**: Resolve >$150M vs. competitors significantly less  
- **Team gap**: Built by leaders from OpenTelemetry, Splunk, DeepMind, Meta  
- **Maturity gap**: Production since 2024 vs. competitors launching in 2025  
- **Investigation gap**: Limited agentic reasoning and cross-stack depth  
- **Enterprise gap**: Compliance and deployment limitations  

**Why Resolve AI**
- Category leader in capital, architecture, and production proof  
- Full-stack AI (models + agents + context + UI)  
- Trusted by enterprises like Coinbase, Zscaler, Salesforce, DoorDash  

---

## Labs / DIY  
*(OpenAI / Claude APIs + Internal Engineering)*

DIY requires owning three continuous loops:

1. **Build**: integrations, orchestration, security, UI  
2. **Operate**: latency, cost, observability  
3. **Improve**: evals, governance, model upgrades  

**Challenges**
- Requires 10–15 engineers, $10M+, 18–24 months  
- Systems degrade with team changes  
- No shared memory or learning  
- Reliability and evaluation are unsolved problems  
- Security and compliance fully owned internally  
- Sequential, human-driven workflows  

**Why Resolve AI**
- Eliminates years of engineering and research effort  
- Provides production-grade reliability and learning systems  
- Outperforms DIY at enterprise scale  