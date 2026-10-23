# AI Governance Lab — Organization Profile Repository (`.github`)

**AI Governance Lab** is an open-source architecture and engineering lab dedicated to building governed, compliant, and scalable Enterprise AI systems across hybrid and multi-cloud environments.

> 📌 **Public Organization Profile:** Rendered from [`profile/README.md`](profile/README.md) at **[https://github.com/AI-Governance-Lab](https://github.com/AI-Governance-Lab)**.

## Architectural Scope

- **Sovereign AI Hubs & LiteLLM Gateways:** Self-hosted Open WebUI, LiteLLM Proxy (`:4000`), Apache Tika OCR, cloud-offloaded RAG, and domain microservices (`private-enterprise-ai-hub`).
- **High-Performance GPU Inference:** NVIDIA NIM, TensorRT-LLM, Triton, vLLM, and Ollama across GCP GPU VMs and K3s/Kubernetes (`nvidia-nim-enterprise-patterns`, `k8s-ollama-fastapi-demo`).
- **Agentic Infrastructure Automation & Multi-Cloud RAG:** Qdrant vector search + guarded Terraform/Ansible execution on AWS EKS, Rancher, and IBM Red Hat OpenShift / PowerVS for SAP S/4HANA (`k8s-ai-agent-multicloud-rag-iac`, `s4hana-ai-agent-openshift`, `k8s-ai-agents-demo`).
- **Quantum-Classical Hybrid Orchestration:** Natural-language-to-circuit compilation (Google Cirq / IBM Qiskit) governed by an independent LLM-as-a-Judge (`governed-quantum-agents`).
- **Google Cloud / Vertex AI Patterns:** Agent Builder, Google ADK, Kubeflow/Vertex AI Pipelines, and serverless Cloud Run inference (`vertex-ai-agentbuilder-demo`, `vertex-ai-pipeline-demo`, `vertex-ai-cloudrun-demo`).
- **Enterprise AI Evaluation, MLOps & Compliance:** Continuous drift monitoring with Evidently AI and experiment/prompt lineage with MLflow 3.x mapped to EU AI Act, NIST AI RMF, ISO/IEC 42001, GDPR, and SOC2 (`k8s-evidently-demo`, `k8s-mlfow-demo`, `k8s-mlflow-rancher-desktop`).

## Repository Families

| Repository | Domain | Availability |
| :--- | :--- | :--- |
| `private-enterprise-ai-hub` | Self-Hosted Enterprise AI Hub, LiteLLM Gateway, Tika OCR & CAD Microservice | 🔒 Private (Public Release Soon) |
| `nvidia-nim-enterprise-patterns` | NVIDIA NIM & TensorRT-LLM Inference Patterns (GCP GPU VMs & K3s/Helm) | 🔒 Private (Public Release Soon) |
| `governed-quantum-agents` | Venus: Quantum-Classical Hybrid Orchestrator + LLM-as-a-Judge | 🌐 Public |
| `k8s-ai-agent-multicloud-rag-iac` | Multi-Cloud RAG + Terraform Runner Agent (Rancher & AWS EKS) | 🌐 Public |
| `s4hana-ai-agent-openshift` | Zero-Touch SAP S/4HANA Provisioning Agent (IBM ROKS, watsonx.ai, PowerVS) | 🌐 Public |
| `k8s-ai-agents-demo` | Reference Kubernetes AI Agent Services (Qdrant, FastAPI, MLflow) | 🌐 Public |
| `vertex-ai-agentbuilder-demo` | Google Vertex AI Agent Builder & Agent Development Kit (ADK) | 🌐 Public |
| `vertex-ai-pipeline-demo` | Vertex AI Pipelines (Kubeflow v2) MLOps Orchestration | 🌐 Public |
| `vertex-ai-cloudrun-demo` | Serverless Vertex AI Embeddings & Gemini Microservices on Cloud Run | 🌐 Public |
| `k8s-evidently-demo` | Evidently AI Drift & Quality Monitoring on Kubernetes | 🌐 Public |
| `k8s-mlfow-demo` | Production MLflow 3.x Cluster Stack (PostgreSQL + MinIO) | 🌐 Public |
| `k8s-mlflow-rancher-desktop` | Local Developer MLflow 3.x Stack on Rancher Desktop (k3s) | 🌐 Public |
| `k8s-ollama-fastapi-demo` | Lightweight Local LLM Serving with Ollama & FastAPI on Kubernetes | 🌐 Public |

## License

Default license is **Apache License 2.0** (see [`LICENSE`](LICENSE) and individual repositories).

---

## Maintainer

**Marian Ropota** — *Hands-On AI/ML & Cloud Platform Architect*  
🔗 [LinkedIn](https://www.linkedin.com/in/marian-rop) • 🏅 [Credly Certifications](https://www.credly.com/users/marian-ropota/badges/credly) • 🐙 [AI Governance Lab](https://github.com/AI-Governance-Lab)