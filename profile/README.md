# AI Governance Lab

Open-source building blocks for end‑to‑end AI governance, secure AI agent deployment, and multi‑cloud MLOps.

## Overview
We curate reproducible patterns that accelerate responsible AI adoption:
- Multi‑cloud & hybrid AI agents (PowerVS, Kubernetes, on‑prem)
- Retrieval Augmented Generation (Qdrant + orchestration)
- Secure image supply chain & hardened base containers
- Infrastructure as Code & composable Helm charts
- ML experiment tracking (MLflow) & lineage
- Model/data quality & drift monitoring (Evidently)
- Lightweight model serving (FastAPI + Ollama)
- Governance by design: traceability, isolation, least privilege

## Featured Repositories
| Area | Repos |
| ---- | ------ |
| Agent Infra & RAG | k8s-ai-agent-multicloud-rag-iac, k8s-ai-agents-demo |
| SAP / PowerVS | ai-agent-s4hana-powervs-deployer |
| Monitoring | k8s-evidently-demo |
| Experiment Tracking | k8s-mlflow-rancher-desktop, k8s-mlflow-demo |
| Serving | k8s-ollama-fastapi-demo |
| GCP / Vertex AI | vertex-ai-cloudrun-demo |

## Architecture Pillars
1. Governance by design (auditability, provenance)
2. Isolation & portability (multi‑cloud ready)
3. Observability & drift detection
4. Supply chain hygiene (minimal, scanned, SBOM)
5. Modularity & composability (small IaC / Helm units)

## Quick Start
1. Select a pattern repo (e.g. k8s-ai-agent-multicloud-rag-iac)
2. Read its README for prerequisites (Kubernetes, credentials, tooling)
3. Build or pull a base image from docker_images_for_ai_agents
4. Deploy via Helm or IaC scripts
5. Enable MLflow + Evidently integrations
6. Extend with additional agents or RAG data sources

## Contribution Guide
- Open an issue before large changes
- Keep modules stateless & parameterized
- Include minimal architecture diagram (PlantUML / Mermaid)
- Provide SBOM or image scan notes for new container images
- Prefer small, reviewable PRs

## Governance & Compliance Readiness
- Reproducible builds (Dockerfiles + pinned deps)
- Supply chain transparency (add SBOM if possible)
- Policy hooks: add admission controls / OPA examples (PRs welcome)
- Observability: expose metrics, logs, drift signals

## Roadmap (Indicative)
- Policy enforcement examples (OPA / Kyverno)
- Extended vector store adapters
- Secure multi‑tenant agent runtime pattern
- CD pipelines with attestations

## Community & Support
- Issues: feature requests / bugs
- Discussions (enable if needed) for design proposals
- Tag PRs with area labels (governance, infra, monitoring, serving)

## Fun Facts
- We like reproducible notebooks more than mystery charts
- Preferred breakfast: immutable artifacts + clean SBOMs

## License
Each repository declares its own license (default: permissive OSS). Review per‑repo LICENSE before use.

Maintained by the AI Governance Lab organization.
