# Findings Log

Narrative findings and recommendations that support the scorecard — cross-cutting issues, one-off risks, and quick wins that don't map cleanly to a single criterion.

Severity: `High` / `Medium` / `Low` — Effort: `Low` / `Medium` / `High` — Status: `Open` / `In Progress` / `Resolved`

| Domain | Finding | Severity | Recommendation | Effort | Owner | Target Date | Status |
|---|---|---|---|---|---|---|---|
| 7. Documentation & Reproducibility | Architecture diagrams reference a feature store that was decommissioned roughly 8 months ago; no current diagram exists. | High | Produce and version-control an up-to-date architecture diagram; require a diagram review as part of major infrastructure changes. | Low | Platform Lead | 2026-10-15 | Open |
| 8. Governance, Risk & Compliance | No documented risk tiering exists to differentiate review rigor between high- and low-stakes models. | High | Adopt a risk-tiering framework (e.g., aligned to NIST AI RMF) and require quarterly review for Tier 1 models. | Medium | Head of Data Science | 2026-11-30 | Open |
| 3. CI/CD & Deployment | Model promotion to production can be performed via a direct registry API call with no required approval step. | Medium | Add a required approval gate (e.g., a protected registry stage transition) before production promotion. | Low | ML Platform Eng | 2026-10-01 | In Progress |
| | | | | | | | |
| | | | | | | | |
| | | | | | | | |
