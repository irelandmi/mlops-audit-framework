# MLOps Audit & Architecture Review Framework

A reusable evaluation framework for MLOps audits and architecture reviews — stack-agnostic, built to be applied to any client.

## Files in this set

| File | Purpose |
|---|---|
| `00-README.md` | This file — methodology and how to use the set |
| `01-domain-weights.md` | The 9 evaluation domains and how they're weighted in the overall score |
| `02-scorecard.md` | The 45-criterion checklist you score during the audit |
| `03-scoring-worksheet.md` | Worksheet for tallying domain scores into an overall maturity score |
| `04-findings-log.md` | Narrative findings and recommendations template |
| `05-evidence-by-tool.md` | Reference: common MLOps tools mapped to the domain(s) they evidence |

## Purpose

This is a standard rubric for evaluating an MLOps program across the full lifecycle — data, model development, deployment, orchestration, monitoring, security, documentation, governance, and organizational process. It is deliberately tool-agnostic: it works whether the client runs Dagster/dbt/MLflow/Snowflake/Azure, SageMaker, Vertex AI, Databricks, or a hand-rolled stack. Use it as the shared methodology across engagements so findings and maturity scores are comparable client to client.

## How to use this set

1. Copy this folder for each new engagement so past clients' work is preserved.
2. Open `01-domain-weights.md` and adjust the weights if this client's risk profile calls for it (see "Adjusting weights" below). Leave equal weights if unsure.
3. Work through `02-scorecard.md`. For each of the 45 criteria, record a score from 0–4 based on evidence you actually collected — not what's documented. Use `05-evidence-by-tool.md` to figure out where to look given this client's specific stack.
4. Log narrative findings that don't fit neatly into a single score — cross-cutting issues, one-off risks, quick wins — in `04-findings-log.md`.
5. Once scored, use `03-scoring-worksheet.md` to tally domain averages and compute an overall weighted maturity score and level.
6. Use the scoring worksheet as the spine of your executive readout, and the scorecard + findings log as the backing detail for the technical debrief.

## Scoring scale (used on every scorecard criterion)

| Score | Level | Description |
|---|---|---|
| 0 | Absent | Not present. No evidence the practice exists in any form. |
| 1 | Ad hoc | Exists informally. Undocumented, inconsistently applied, dependent on individual habits. |
| 2 | Defined | A documented process exists but is manual or inconsistently followed in practice. |
| 3 | Managed | Implemented, mostly automated, and actively tracked with some monitoring or reporting. |
| 4 | Optimized | Fully automated, continuously monitored, and embedded as standard practice with periodic review. |

## Adjusting weights for different client types

- **Regulated (finance, healthcare, insurance):** increase weight on *Governance, Risk & Compliance* and *Security & Access Control* — these clients are usually judged against SR 11-7/SR 26-2, the EU AI Act, or ISO/IEC 42001.
- **Early-stage / single-team:** increase weight on *CI/CD & Deployment* and *Monitoring & Observability*, where technical debt accumulates fastest; governance maturity is often appropriately low at this stage.
- **Due-diligence / M&A engagements:** keep weights close to equal so the resulting score is a defensible, broad-based maturity signal rather than one tuned to a single risk lens.

## The 9 evaluation domains

1. Data & Pipeline Governance
2. Model Development & Experimentation
3. CI/CD & Deployment
4. Orchestration & Reliability
5. Monitoring & Observability
6. Security & Access Control
7. Documentation & Reproducibility
8. Governance, Risk & Compliance
9. Organizational & Process Maturity
