# Scorecard

Score each criterion 0–4 using the scale in `00-README.md`. Fill in the blank cells in the **Score** and **Notes / Findings** columns as you collect evidence. Use `05-evidence-by-tool.md` to map criteria to where evidence lives in this client's specific stack.

---

## 1. Data & Pipeline Governance

| Criterion | What to Evaluate | Example Evidence to Request | Score (0–4) | Notes / Findings |
|---|---|---|---|---|
| Data lineage traceability | Can a prediction or output be traced back to the exact source data, transformation steps, and version that produced it? | Lineage graph (e.g., dbt DAG, Dagster asset graph); a sample end-to-end trace of one prediction | | |
| Data versioning & snapshotting | Are raw and processed datasets versioned or snapshotted so a training run can be reproduced against the exact data used? | Data version tags; snapshot/time-travel config (e.g., Snowflake Time Travel, Delta Lake, DVC) | | |
| Data quality validation | Are automated checks (schema, null/range, distribution) run before data enters training or serving? | Test suite results (e.g., dbt tests, Great Expectations, Deequ); CI logs | | |
| Data access controls & PII handling | Is access to sensitive data role-gated, and is PII masked or classified? | RBAC/grant configuration; masking policies; data classification tags | | |
| Data documentation & ownership | Are data sources, transformations, and owners documented and discoverable? | Data catalog entries; dbt docs/exposures; ownership registry | | |

## 2. Model Development & Experimentation

| Criterion | What to Evaluate | Example Evidence to Request | Score (0–4) | Notes / Findings |
|---|---|---|---|---|
| Experiment tracking | Are training runs, hyperparameters, metrics, and artifacts systematically logged? | Experiment tracker records (e.g., MLflow runs, W&B); sample run history | | |
| Training reproducibility | Can a model be retrained from the same code, data, and config to produce a comparable result? | Environment/dependency pinning; containerized training jobs; a reproducibility test result | | |
| Pre-promotion model validation | Are new models evaluated against holdout data, a baseline, and fairness/bias checks before promotion? | Evaluation reports; bias test results; baseline comparison logs | | |
| Model versioning & registry | Are trained models registered with metadata and clear stage transitions (dev/staging/prod)? | Model registry entries (e.g., MLflow Model Registry); version/stage history | | |
| Training code review & testing | Is training code peer-reviewed and covered by unit/integration tests? | PR history; test coverage reports; CI pipeline config | | |

## 3. CI/CD & Deployment

| Criterion | What to Evaluate | Example Evidence to Request | Score (0–4) | Notes / Findings |
|---|---|---|---|---|
| Deployment automation level | Is model deployment manual, semi-automated, or fully CI/CD-driven? | Deployment pipeline definitions; recent deployment logs | | |
| Promotion approval gates | Is there a required, auditable approval step before a model reaches production? | Approval workflow config; registry stage-transition permissions | | |
| Rollback capability | Can a prior model or pipeline version be restored quickly if a deployment fails? | Rollback procedure; record of a past rollback | | |
| Safe rollout practices | Are new models rolled out via canary, shadow, or A/B mechanisms rather than a full cutover? | Rollout configuration; traffic-split logs | | |
| Environment parity | Are dev, staging, and production environments consistent in dependencies, config, and containerization? | Container/image definitions; environment diff report | | |

## 4. Orchestration & Reliability

| Criterion | What to Evaluate | Example Evidence to Request | Score (0–4) | Notes / Findings |
|---|---|---|---|---|
| Scheduling & trigger reliability | Do scheduled or triggered pipeline runs execute reliably, and are missed runs detected? | Orchestrator run history (e.g., Dagster, Airflow); SLA/freshness reports | | |
| Retry & failure handling | Do pipelines retry transient failures automatically and handle persistent failures gracefully? | Retry policy config; failure logs | | |
| Failure alerting | Are pipeline owners notified in near real time when a run fails? | Alert/notification configuration; on-call records | | |
| Dependency management | Are pipeline/asset dependencies explicitly declared and enforced rather than implicit? | DAG or asset graph definitions | | |
| Backfill & reprocessing capability | Can historical data be reprocessed reliably when logic or data changes? | Backfill run history; partition reprocessing config | | |

## 5. Monitoring & Observability

| Criterion | What to Evaluate | Example Evidence to Request | Score (0–4) | Notes / Findings |
|---|---|---|---|---|
| Data drift detection | Is input/feature distribution monitored for drift relative to training data? | Drift monitoring dashboards/alerts (e.g., Evidently, Fiddler, Arize) | | |
| Model performance monitoring | Are live model performance or business KPIs tracked against expectations? | Monitoring dashboards; alert thresholds | | |
| Model staleness tracking | Is model age tracked with alerts before performance decay becomes business-impacting? | Staleness/age monitoring configuration | | |
| Infrastructure monitoring | Are latency, resource usage, and serving costs monitored? | Infra dashboards (e.g., Azure Monitor, Datadog); cost reports | | |
| Ground-truth feedback loop | Are outcome labels captured and fed back to evaluate and retrain models? | Feedback capture pipeline; label-latency metrics | | |

## 6. Security & Access Control

| Criterion | What to Evaluate | Example Evidence to Request | Score (0–4) | Notes / Findings |
|---|---|---|---|---|
| Role-based access control | Is least-privilege access enforced consistently across data, compute, and registry tools? | RBAC/IAM policy exports; access review records | | |
| Secrets management | Are credentials and secrets stored in a vault rather than hardcoded or in plain config? | Secrets manager usage (e.g., Azure Key Vault); config scan results | | |
| Network & infrastructure isolation | Is sensitive infrastructure segmented or isolated appropriately? | Network topology; security group/firewall rules | | |
| Audit logging | Is there immutable, queryable logging of who did what and when across the platform? | Audit log samples; retention policy | | |
| Dependency & vulnerability management | Are ML dependencies and containers scanned for known vulnerabilities? | Scan reports; patch cadence records | | |

## 7. Documentation & Reproducibility

| Criterion | What to Evaluate | Example Evidence to Request | Score (0–4) | Notes / Findings |
|---|---|---|---|---|
| Architecture documentation currency | Does current architecture documentation match what's actually deployed? | Architecture diagrams compared against live pipeline configs | | |
| Operational runbooks | Are there runbooks for common operational and incident scenarios? | Runbook repository; on-call handoff notes | | |
| Model documentation (model cards) | Is each production model documented with purpose, training data, limitations, and intended use? | Sample model cards | | |
| Onboarding documentation | Could a new team member operate the system from documentation alone? | Onboarding guide; new-hire feedback | | |
| Design decision records | Are significant architecture or design decisions recorded with rationale? | ADRs or an equivalent decision log | | |

## 8. Governance, Risk & Compliance

| Criterion | What to Evaluate | Example Evidence to Request | Score (0–4) | Notes / Findings |
|---|---|---|---|---|
| Regulatory mapping | Have applicable regulations or standards (e.g., EU AI Act, sector model-risk rules) been mapped to system risk tiers? | Risk assessment/tiering documentation | | |
| Human oversight for high-risk decisions | Is there a defined, working escalation or override path for high-stakes automated decisions? | Escalation procedure; sample override log | | |
| Bias & fairness testing | Is bias/fairness testing performed and documented for models affecting people? | Fairness test reports | | |
| Differentiated review cadence by risk | Do higher-risk models receive more frequent or rigorous review than low-risk ones? | Review calendar; risk-tiered governance policy | | |
| Third-party/vendor model risk management | Are externally sourced models or APIs assessed and monitored for risk? | Vendor risk assessments; SLA/monitoring for third-party endpoints | | |

## 9. Organizational & Process Maturity

| Criterion | What to Evaluate | Example Evidence to Request | Score (0–4) | Notes / Findings |
|---|---|---|---|---|
| Clear ownership | Does every pipeline or model have a named owner accountable for it? | Ownership registry; RACI matrix | | |
| Change management process | Are changes to production ML systems reviewed and approved through a defined process? | PR/change-approval history | | |
| Incident response process | Is there a defined process for responding to model or pipeline incidents? | Incident response plan; past incident postmortems | | |
| Cross-functional alignment | Do data engineering, ML engineering, and compliance/risk functions coordinate effectively? | Meeting cadence; shared planning artifacts | | |
| Continuous improvement cadence | Does the team periodically reassess and improve MLOps maturity (e.g., retrospectives, repeat audits)? | Retrospective notes; prior audit follow-through | | |
