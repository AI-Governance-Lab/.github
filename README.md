# AI Governance Lab

A collection of open source assets demonstrating end‑to‑end AI governance, secure AI agent deployment, and multi‑cloud MLOps patterns.

## Scope

- Multi‑cloud AI agents: reusable deployment patterns (PowerVS, Kubernetes, hybrid).
- Retrieval Augmented Generation (RAG): infra + vector DB (Qdrant) + orchestration.
- Secure container build & delivery: scripts and base images under `docker_images_for_ai_agents`.
- Infrastructure as Code: Kubernetes clusters, Helm charts, IaC modules (`k8s-*`, `ai-agent-s4hana-powervs-deployer`).
- MLOps & Experiment Tracking: MLflow demos (`k8s-mlflow-*`).
- Model & Data Quality Monitoring: Evidently integration (`k8s-evidently-demo`).
- Fast API + model serving examples (`k8s-ollama-fastapi-demo`).
- Governance foundations: reproducibility, environment isolation, observability, policy readiness.

## Repository Families

- ai-agent-s4hana-powervs-deployer: PowerVS + SAP integration deployment automation.
- docker_images_for_ai_agents: Curated base images for governed AI workloads.
- k8s-ai-agent-multicloud-rag-iac: RAG + agents infra as code.
- k8s-ai-agents-demo: Reference agent scenarios.
- k8s-evidently-demo: Monitoring & drift detection.
- k8s-mlflow-rancher-desktop / k8s-mlfow-demo: Local & cluster MLflow patterns.
- k8s-ollama-fastapi-demo: Lightweight model serving.

## Principles

1. Governance by design: traceability, versioning, auditability.
2. Isolation & portability: multi-cloud ready artifacts.
3. Observability: metrics, drift, lineage.
4. Least privilege & supply chain hygiene.
5. Modularity: composable Helm charts / IaC units.

## Getting Started

1. Pick a stack folder (e.g. `k8s-ai-agent-multicloud-rag-iac`).
2. Review README in that folder for prerequisites.
3. Build or pull the required base image from `docker_images_for_ai_agents`.
4. Deploy via Helm / IaC.
5. Extend with monitoring (Evidently) and tracking (MLflow).

## Contributing

- Open issues for enhancements.
- Keep modules stateless & parameterized.
- Provide architecture diagrams when adding new vertical capabilities.

## License

Each subfolder contains its license; default is permissive OSS (see included LICENSE files).

---

Maintained by the AI Governance Lab organization.