# Scoring Worksheet

Use this after completing `02-scorecard.md` to roll the 45 criterion scores up into domain averages and an overall maturity score.

## Step 1 — Domain averages

For each domain, average its 5 criterion scores from the scorecard (sum ÷ 5).

| Domain | Avg Score (0–4) | Weight (from `01-domain-weights.md`) | Weighted Contribution (Avg × Weight) |
|---|---|---|---|
| 1. Data & Pipeline Governance | | | |
| 2. Model Development & Experimentation | | | |
| 3. CI/CD & Deployment | | | |
| 4. Orchestration & Reliability | | | |
| 5. Monitoring & Observability | | | |
| 6. Security & Access Control | | | |
| 7. Documentation & Reproducibility | | | |
| 8. Governance, Risk & Compliance | | | |
| 9. Organizational & Process Maturity | | | |
| **Overall Weighted Maturity Score** | | | **Sum of the Weighted Contribution column** |

## Step 2 — Maturity level

Look up the Overall Weighted Maturity Score (0–4 scale) against this table:

| Score range | Maturity Level |
|---|---|
| < 1.0 | Level 0 — Initial / Absent |
| 1.0 – < 2.0 | Level 1 — Ad hoc |
| 2.0 – < 3.0 | Level 2 — Defined |
| 3.0 – < 3.5 | Level 3 — Managed |
| ≥ 3.5 | Level 4 — Optimized |

**Overall Maturity Level:** _______________

**Overall Maturity (%):** Overall Weighted Maturity Score ÷ 4 = _______________

## Step 3 — Risk summary

Count criteria from the scorecard (45 total) that fall into each bucket:

| Bucket | Count |
|---|---|
| High Risk (score 0–1) | |
| Medium Risk (score 2) | |
| Low Risk (score 3–4) | |
| Not yet scored | |

## Step 4 — Executive summary

Use these rolled-up numbers as the spine of the executive readout:

- Lead with the Overall Maturity Level and what it means in plain language.
- Call out the 2–3 lowest-scoring domains and how many High Risk criteria sit within them.
- Reference specific findings from `04-findings-log.md` to ground each low score in concrete evidence.
- Note any domain where the weight was adjusted for this client and why (e.g., Governance weighted higher for a regulated client).
