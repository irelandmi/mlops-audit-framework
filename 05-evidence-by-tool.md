# Evidence by Tool

Reference: common MLOps stack components mapped to the domain(s) they primarily provide evidence for. Not exhaustive — use it to orient quickly on an unfamiliar stack, then adapt to whatever the client actually runs.

| Category | Example Tools | Primarily Evidences |
|---|---|---|
| Orchestration | Dagster, Airflow, Prefect, Azure Data Factory | 4. Orchestration & Reliability; 1. Data & Pipeline Governance (lineage) |
| Transformation / Analytics Engineering | dbt, Spark SQL | 1. Data & Pipeline Governance; 7. Documentation & Reproducibility (dbt docs) |
| Experiment Tracking & Model Registry | MLflow, Weights & Biases, Neptune, SageMaker Model Registry, Vertex AI Model Registry | 2. Model Development & Experimentation; 3. CI/CD & Deployment |
| Data Warehouse / Lakehouse | Snowflake, Databricks/Delta Lake, BigQuery, Redshift | 1. Data & Pipeline Governance; 6. Security & Access Control |
| Cloud / Infra Platform | Azure (IAM, Key Vault, Monitor), AWS, GCP | 6. Security & Access Control; 5. Monitoring & Observability |
| Data Quality | Great Expectations, dbt tests, Deequ, Soda | 1. Data & Pipeline Governance |
| Monitoring / Observability | Evidently AI, Fiddler, Arize, Datadog, Azure Monitor | 5. Monitoring & Observability |
| Feature Store | Feast, Databricks Feature Store, Tecton | 1. Data & Pipeline Governance; 2. Model Development & Experimentation |
| CI/CD | GitHub Actions, GitLab CI, Jenkins, Azure DevOps | 3. CI/CD & Deployment; 9. Organizational & Process Maturity (change management) |
| Data Versioning | DVC, LakeFS, Delta Lake time travel, Snowflake Time Travel | 1. Data & Pipeline Governance; 2. Model Development & Experimentation (reproducibility) |
