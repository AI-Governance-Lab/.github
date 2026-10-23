# AI Governance Lab

> **Hands-On Enterprise AI Engineering, Production Code & Reference Deployments**  
> Not Just Architecture Diagrams — Executable Codebases, Microservices, Terraform/Ansible IaC, Helm Charts & Live Multi-Cloud Deployments

[![License](https://img.shields.io/badge/License-Apache_2.0-22C55E?style=flat-square)](LICENSE)
[![Focus](https://img.shields.io/badge/Focus-Hands--On_AI_Engineering_%26_Architecture-7B42BC?style=flat-square)]()
[![Execution](https://img.shields.io/badge/Deliverables-Working_Code_%2B_Automated_Deployments-0EA5E9?style=flat-square)]()
[![Governance](https://img.shields.io/badge/Compliance-EU_AI_Act_%7C_NIST_RMF_%7C_ISO_42001_%7C_SOC2-F59E0B?style=flat-square)]()
[![LinkedIn](https://img.shields.io/badge/Maintainer-Marian_Ropota_(LinkedIn)-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/marian-rop)
[![Credly](https://img.shields.io/badge/Certifications-Credly_Verified-FF6B00?style=flat-square&logo=credly)](https://www.credly.com/users/marian-ropota/badges/credly)

**AI Governance Lab** is a **hands-on open-source engineering and architecture lab** founded and maintained by **[Marian Ropota](https://www.linkedin.com/in/marian-rop)** (*AI/ML & Cloud Platform Architect*). Unlike theoretical architecture portfolios, every repository in this lab combines **system design** with **working application code (Python, FastAPI, Asyncio, LangGraph, ADK)** and **automated infrastructure deployment (Terraform, Ansible, Helm, Kubernetes, Docker/Podman)**.

We build, deploy, and benchmark real-world **MLOps**, **LLMOps**, **Autonomous AI Agents**, and **Hybrid/Multi-Cloud Platforms** with built-in **AI Governance**, **LLM-as-a-Judge evaluation**, and **regulatory compliance** (EU AI Act, NIST AI RMF, ISO/IEC 42001, GDPR, SOC2, HIPAA) across **Google Cloud (Vertex AI, BigQuery, GKE, Cloud Run)**, **IBM Cloud (watsonx.ai, OpenShift/ROKS, PowerVS)**, **AWS (EKS, Bedrock)**, **Azure**, and **On-Premises (Rancher, K3s, OpenStack)**.

*Keywords: AI Governance, Enterprise AI Architecture, MLOps, LLMOps, Agentic Workflows, LiteLLM, NVIDIA NIM, TensorRT-LLM, Triton, vLLM, LLM-as-a-Judge, LangGraph, Google ADK, Model Context Protocol (MCP), RAG, Qdrant, Kubernetes, OpenShift, OpenStack, Terraform, Argo CD, Quantum AI, EU AI Act, GDPR, SOC2*

---

## 🏛️ System-Level Reference Architecture

```mermaid
C4Context
    title AI Governance Lab — Enterprise AI & Hybrid Cloud Reference Architecture

    Person(operator, "Platform Architect / Engineer / Operator", "Designs blueprints, executes via GitOps & IaC, monitors compliance")

    System_Boundary(governance, "Governance & Evaluation Plane (Cross-Cutting)") {
        System(judge, "LLM-as-a-Judge & AI Evaluation", "Onboarding gates, hallucination, bias & safety scoring")
        System(opa, "Policy-as-Code (OPA / Kyverno)", "Admission control, guardrails & resource policies")
        System(evidently, "Evidently AI", "Data drift, model quality & compliance dashboards")
        System(mlflow, "MLflow 3.x", "Experiment tracking, prompt/model registry & lineage")
        System(supply, "Supply Chain & Resilience", "Cosign, SBOM, Trivy, automated platform resilience")
    }

    System_Boundary(gateway, "Sovereign AI Workspace & Gateway Plane") {
        System(hub, "Enterprise AI Hub (Open WebUI + Tools)", "Self-hosted RAG, Apache Tika OCR & domain microservices")
        System(litellm, "LiteLLM Proxy Gateway", "AI FinOps, centralized auth, fallback routing & model governance")
    }

    System_Boundary(ai, "AI Workloads & High-Performance Inference Plane") {
        System(nim, "NVIDIA NIM / Triton / TensorRT-LLM", "GPU-optimized inference on L4 / A100 / H100")
        System(vllm, "vLLM / Ollama", "High-throughput & lightweight local model serving")
        System(cloud_llm, "Cloud Foundation Models", "Vertex AI (Gemini), IBM watsonx.ai, Bedrock, Mistral, OpenRouter")
    }

    System_Boundary(data, "Data, RAG & Lakehouse Plane") {
        System(qdrant, "Qdrant Vector DB", "Private embeddings, hybrid semantic search")
        System(gcp_data, "Cloud Data & ML Pipelines", "BigQuery, Dataflow, Pub/Sub, Vertex AI Pipelines, Lakehouse")
    }

    System_Boundary(control, "Control & Infrastructure Plane (Multi-Cloud & On-Prem)") {
        System(k8s, "Kubernetes & OpenShift", "AWS EKS, GCP GKE, IBM ROKS, Rancher, K3s")
        System(iac, "Agentic IaC & GitOps", "LangGraph Toolbelt, Terraform, Ansible, Argo CD")
        System(infra, "Enterprise Targets", "IBM PowerVS (SAP S/4HANA), GCP GPU VMs, OpenStack NFVI")
    }

    System_Boundary(quantum, "Quantum-Classical Plane") {
        System(venus, "Venus (Governed Quantum Agents)", "NL-to-Circuit translation + Cirq / Qiskit execution")
    }

    Rel(operator, hub, "Interacts & orchestrates via")
    Rel(hub, litellm, "Routes chat & RAG embeddings")
    Rel(litellm, ai, "Load balances & enforces budgets")
    Rel(ai, data, "Grounded retrieval & pipelines")
    Rel(control, ai, "Schedules & scales workloads")
    Rel(control, infra, "Provisions via Terraform/Ansible/GitOps")
    Rel(quantum, judge, "Validates scientific & policy compliance")
    Rel(governance, ai, "Evaluates & monitors")
    Rel(governance, control, "Enforces policies & audit trails")
```

### 🔐 Cross-Cutting Governance Layers

| Layer | Technologies | Architectural Purpose |
| :--- | :--- | :--- |
| **AI Evaluation & Onboarding** | LLM-as-a-Judge, Custom Eval Suites, Pydantic v2 | Pre-production quality gates, schema enforcement, hallucination & toxicity checks |
| **Data & Model Monitoring** | Evidently AI, Prometheus, Grafana | Continuous drift detection, data quality reports, post-market compliance evidence |
| **Experiment & Lineage Tracking** | MLflow 3.x, PostgreSQL, MinIO (S3) | Prompt/model versioning, reproducibility, approval stages, immutable audit trail |
| **Policy-as-Code & Security** | OPA / Gatekeeper, Kyverno, RBAC, NetworkPolicies | Kubernetes admission control, tenant isolation, least-privilege IAM |
| **AI FinOps & Gateway Control** | LiteLLM Proxy, Token/Cost Budgets, Fallback Routing | Multi-provider resilience, data residency routing (Cloud vs. Local GPU), cost governance |

---

## 🚀 Featured Repositories by Architectural Domain

### 1. 🏢 Sovereign AI Workspace & Multi-Model LiteLLM Gateway

**[private-enterprise-ai-hub](https://github.com/AI-Governance-Lab/private-enterprise-ai-hub)** — *Self-Hosted Enterprise AI Hub & LiteLLM Gateway* · `🔒 Private — Public Release Coming Soon`  
Self-hosted AI workspace combining **Open WebUI**, **LiteLLM Proxy (`:4000`)**, **Apache Tika OCR**, **cloud-offloaded RAG (`text-embedding-004`)**, and isolated domain microservices (FastAPI `.dwg`/`.dxf` ⇄ `.xlsx` engineering reconciliation) routing across Google Vertex AI (Gemini), Mistral (Codestral / Ministral), NVIDIA NIM, and OpenRouter while keeping all documents and chat history on local redundant storage.  
*Technologies: LiteLLM, Open WebUI, FastAPI, Vertex AI, Mistral, NVIDIA NIM, Apache Tika, Podman/Docker, Systemd*

### 2. ⚡ High-Performance GPU Inference at Scale

**[nvidia-nim-enterprise-patterns](https://github.com/AI-Governance-Lab/nvidia-nim-enterprise-patterns)** — *NVIDIA NIM & TensorRT-LLM Enterprise Reference Architecture* · `🔒 Private — Public Release Coming Soon`  
Bridges GPU infrastructure provisioning and production LLM serving across two tiers: **Tier 1** (Docker on ephemeral GCP Spot GPU VMs via Terraform for rapid benchmarking) and **Tier 2** (K3s + Helm + shared PVC model cache for HA enterprise orchestration). Includes hardware profiling (L4/T4/H100 ↔ 7B/8B/70B models) and verified live benchmarks (`deepseek-r1-distill-llama-8b` on NVIDIA L4 24GB: 95.8% VRAM utilization, <25s warm start).  
*Technologies: NVIDIA NIM, TensorRT-LLM, Triton, K3s, Helm, Terraform, GCP GPU VMs, Python*

**[k8s-ollama-fastapi-demo](https://github.com/AI-Governance-Lab/k8s-ollama-fastapi-demo)** — *Cloud-Native Local LLM Serving Pattern*  
Containerized AI inference microservice integrating **FastAPI** and **Ollama** on Kubernetes, designed as a lightweight, air-gapped-ready serving template with hooks for MLflow, Evidently, and OPA governance.  
*Technologies: FastAPI, Ollama, Kubernetes, Docker, Python*

### 3. 🤖 Agentic Infrastructure Automation & Multi-Cloud RAG

**[k8s-ai-agent-multicloud-rag-iac](https://github.com/AI-Governance-Lab/k8s-ai-agent-multicloud-rag-iac)** — *RAG-Powered Multi-Cloud Terraform Agent on Kubernetes*  
Production-validated Kubernetes AI agent combining private document RAG (**Qdrant**) with an automated **Terraform Runner** executing Kubernetes Jobs across **AWS, Azure, GCP, and IBM Cloud**. Validated on **Rancher (on-prem)** and **AWS EKS** (EFS RWX, EBS gp3, ALB Controller, Route 53) with multi-provider LLM support (OpenAI, Azure OpenAI, AWS Bedrock, Ollama).  
*Technologies: Kubernetes, AWS EKS, Rancher, Terraform, Helm, FastAPI, LangChain/LangGraph, Qdrant, Bedrock*

**[s4hana-ai-agent-openshift](https://github.com/AI-Governance-Lab/s4hana-ai-agent-openshift)** — *Zero-Touch SAP S/4HANA Provisioning Agent on OpenShift & IBM PowerVS*  
Agentic infrastructure automation platform running on **IBM Red Hat OpenShift (ROKS)** powered by **IBM watsonx.ai** and **Qdrant RAG**. Translates natural-language infrastructure requests into guarded **Terraform** runs targeting **IBM Cloud PowerVS** for SAP S/4HANA landing zones, streaming real-time execution logs back to the operator UI.  
*Technologies: Red Hat OpenShift (ROKS), IBM watsonx.ai, IBM PowerVS, SAP S/4HANA, Terraform, Qdrant, FastAPI, Helm*

**[k8s-ai-agents-demo](https://github.com/AI-Governance-Lab/k8s-ai-agents-demo)** — *Kubernetes AI Agent Reference Wiring*  
Reference implementation for containerized AI agent services on Kubernetes with Qdrant vector search, FastAPI endpoints, and integrated hooks for MLflow experiment tracking and Evidently drift monitoring.  
*Technologies: Kubernetes, Docker, Qdrant, IBM watsonx, MLflow, Evidently AI, FastAPI*

### 4. ⚛️ Quantum-Classical Hybrid Orchestration

**[governed-quantum-agents](https://github.com/AI-Governance-Lab/governed-quantum-agents)** — *Venus: Governed Quantum Agents (GQA)*  
Bloat-free, enterprise-grade multi-agent orchestrator (`Python asyncio` + `Pydantic v2` + `LiteLLM`) that translates natural-language scientific discovery goals into quantum algorithms (**VQE, QAOA, QSVM, Grover**) and executable circuits (**Google Cirq & IBM Qiskit**). Guarded by an independent **LLM-as-a-Judge** agent verifying scientific validity and regulatory compliance.  
*Technologies: Quantum Computing, Google Cirq, IBM Qiskit, Python Asyncio, Pydantic v2, LiteLLM, Gemini, vLLM, FastAPI*

### 5. ☁️ Google Cloud Data & Vertex AI Platforms

**[vertex-ai-agentbuilder-demo](https://github.com/AI-Governance-Lab/vertex-ai-agentbuilder-demo)** — *Vertex AI Agent Builder & Google ADK Patterns*  
Programmatic and low-code agent architectures using **Google Vertex AI Agent Builder**, **Agent Engine (Reasoning Engine)**, and the **Agent Development Kit (ADK)** with custom tool execution and Cloud Run / Agent Engine deployment workflows.  
*Technologies: Google Vertex AI, Google ADK, Reasoning Engine, Gemini, Cloud Run, Docker*

**[vertex-ai-pipeline-demo](https://github.com/AI-Governance-Lab/vertex-ai-pipeline-demo)** — *Cloud-Native MLOps Pipeline Orchestration*  
Kubeflow Pipelines v2 (`kfp`) workflows compiled and executed on **Google Vertex AI Pipelines** for reproducible, parameterized ML training, evaluation, and artifact lineage on GCS.  
*Technologies: Vertex AI Pipelines, Kubeflow (KFP v2), Google Cloud Storage, Python, MLOps*

**[vertex-ai-cloudrun-demo](https://github.com/AI-Governance-Lab/vertex-ai-cloudrun-demo)** — *Serverless Vertex AI Microservices*  
Portable, scale-to-zero Python microservices exposing **Vertex AI Embeddings (`text-embedding-004`)** and **Gemini 2.5 Pro** endpoints via Docker Hub, GCR, and Artifact Registry on **Google Cloud Run**.  
*Technologies: Google Cloud Run, Vertex AI, Gemini, Artifact Registry, Docker, Flask*

### 6. 🛡️ Enterprise AI Evaluation, MLOps & Regulatory Monitoring

**[k8s-evidently-demo](https://github.com/AI-Governance-Lab/k8s-evidently-demo)** — *Continuous AI Quality & Drift Monitoring on Kubernetes*  
Kubernetes deployment of **Evidently AI** generating operational compliance evidence, data drift reports, and model quality dashboards mapped directly to **EU AI Act**, **NIST AI RMF 1.0**, **ISO/IEC 42001**, and **GDPR** requirements.  
*Technologies: Evidently AI, Kubernetes, Prometheus, Grafana, EU AI Act, NIST AI RMF, ISO 42001*

**[k8s-mlfow-demo](https://github.com/AI-Governance-Lab/k8s-mlfow-demo)** — *Cluster MLOps & LLMOps Tracking Stack (MLflow 3.x)*  
Production-ready Helm deployment of **MLflow 3.3+** on Kubernetes with **PostgreSQL** tracking backend and **MinIO (S3)** artifact store for LLM prompt/config tracking, evaluation comparisons, and Model Registry governance.  
*Technologies: MLflow 3.x, Kubernetes, Helm, PostgreSQL, MinIO, LLMOps*

**[k8s-mlflow-rancher-desktop](https://github.com/AI-Governance-Lab/k8s-mlflow-rancher-desktop)** — *Local Developer MLOps Sandbox on Rancher Desktop (k3s)*  
Single-command local MLOps/LLMOps stack running MLflow 3.x, PostgreSQL, and MinIO on **Rancher Desktop (k3s)** for rapid, isolated experimentation before cluster promotion.  
*Technologies: MLflow 3.x, Rancher Desktop, k3s, Helm, PostgreSQL, MinIO*

---

## 📦 Capabilities & Compliance Matrix

| Capability | `private-enterprise-ai-hub` | `nvidia-nim-enterprise-patterns` | `k8s-ai-agent-multicloud-rag-iac` | `s4hana-ai-agent-openshift` | `governed-quantum-agents` | `k8s-evidently` & `k8s-mlflow-*` | `vertex-ai-*` |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **RAG & Document Intelligence** | ✅ (Tika OCR + Vertex) | ❌ | ✅ (Qdrant RWX) | ✅ (SAP Docs) | ✅ (Quantum Domain) | ❌ | ✅ |
| **Agentic Tool Execution** | ✅ (CAD Microservice) | ❌ | ✅ (Terraform Jobs) | ✅ (PowerVS IaC) | ✅ (Cirq / Qiskit) | ❌ | ✅ (ADK) |
| **LiteLLM / Multi-Model Routing** | ✅ (LiteLLM :4000) | ❌ | ✅ (Multi-Provider) | ❌ | ✅ (Core) | ❌ | ❌ |
| **LLM-as-a-Judge / Eval Gates** | 🔄 | ✅ (Test Suite) | 🔄 | 🔄 | ✅ (Core Judge) | ✅ (MLflow Eval) | ❌ |
| **Drift & Lineage Observability** | ❌ | ✅ (GPU Telemetry) | ✅ (Addon Ready) | 🔄 | ❌ | ✅ (Core) | ✅ (Pipelines) |
| **Multi-Cloud / Hybrid IaC** | ✅ (Podman/Systemd) | ✅ (GCP + K3s) | ✅ (AWS/Azure/GCP/IBM) | ✅ (ROKS + PowerVS) | ✅ (Docker/FastAPI) | ✅ (Helm/K8s) | ✅ (Cloud Run) |

### ⚖️ Regulatory & Framework Alignment

| Framework / Standard | Technical Controls Implemented Across Repositories |
| :--- | :--- |
| **EU AI Act & ISO/IEC 42001** | Pre-deployment LLM-as-a-Judge risk & hallucination evaluation (`governed-quantum-agents`), continuous post-market drift monitoring (`k8s-evidently-demo`), and versioned model/prompt lineage (`k8s-mlfow-demo`). |
| **NIST AI RMF 1.0** | *Govern, Map, Measure, Manage* functions operationalized via Policy-as-Code (OPA/Kyverno), structured Pydantic v2 I/O schemas, and automated evaluation pipelines. |
| **GDPR & Data Sovereignty** | Local RAID/PVC data residency (`private-enterprise-ai-hub`), namespace/tenant isolation, air-gapped or private GPU inference (`nvidia-nim-enterprise-patterns`, `vLLM`, `Ollama`), zero secrets in images. |
| **SOC2 & Supply Chain Security** | Declarative GitOps delivery (Argo CD / Helm), least-privilege Service Accounts, container hardening, SBOM/Trivy scanning, and immutable execution logs. |

---

## 🏛️ Architectural Principles

- **🎯 Blueprint-to-Code Execution:** Every reference architecture is paired with executable Terraform modules, Helm charts, Docker/Podman definitions, and automated validation scripts.
- **🤖 Unified AI Gateway & FinOps Control:** Centralized LiteLLM proxy plane managing multi-provider authentication, fallback meshes, and token/cost budgets across cloud and local GPU models.
- **🛡️ Governance by Design:** Evaluation gates, schema validation, drift detection, and audit logging are embedded into the runtime architecture—not bolted on after deployment.
- **🌐 Hybrid & Multi-Cloud Portability:** Workload mobility across hyperscalers (GCP, IBM Cloud, AWS, Azure) and on-premises/edge infrastructure (OpenShift, Rancher, K3s, OpenStack).
- **⚡ Performance & Resource Efficiency:** Hardware-profiled GPU inference (TensorRT-LLM / NIM / vLLM) combined with cloud-offloaded embeddings and scale-to-zero serverless patterns.

---

## 🌍 Industry Reference Blueprints

- **📡 Telecommunications & Cloud Infrastructure:** Enterprise AI evaluation & onboarding frameworks, multi-cluster Kubernetes/OpenStack orchestration, and automated platform resilience.
- **🏦 Financial Services & Insurance:** Governed RAG and agentic workflows with full audit lineage (MLflow + Evidently), data platform modernization patterns, and quantum-assisted portfolio/fraud analysis.
- **🏭 Enterprise ERP & Manufacturing (SAP S/4HANA):** Zero-touch SAP infrastructure provisioning on IBM Cloud PowerVS and Red Hat OpenShift via guarded AI agents and Terraform/Ansible automation.
- **🛒 Retail & Document-Heavy Operations:** Cloud-native analytics pipelines (BigQuery, Dataflow, Vertex AI), OCR document intelligence (Apache Tika), and automated CAD/tabular reconciliation microservices.
- **🛡️ Cybersecurity & Life Sciences:** Quantum Grover log search simulations, HIPAA/GDPR-isolated RAG deployments, and zero-trust container supply chains.

---

## 🧰 Technology Stack

- **Cloud & Virtualization:** Google Cloud (Vertex AI, BigQuery, Dataflow, Pub/Sub, Cloud Run, GKE), IBM Cloud (watsonx.ai, ROKS/OpenShift, PowerVS), AWS (EKS, Bedrock, EFS/EBS/ALB), Azure, OpenStack, VMware/KVM
- **Container & GitOps Orchestration:** Kubernetes, Red Hat OpenShift, Rancher, K3s, Helm, Argo CD, Docker, Podman, Systemd
- **Infrastructure as Code:** Terraform, Ansible, Cloud Build
- **AI Inference & Gateways:** NVIDIA NIM, TensorRT-LLM, Triton, NeMo, vLLM, Ollama, LiteLLM Proxy, OpenRouter
- **Foundation Models:** Google Gemini, IBM watsonx, OpenAI, Anthropic Claude, Mistral (Codestral / Ministral), DeepSeek, NVIDIA Nemotron, Zhipu GLM
- **Agentic Frameworks & Developer Tooling:** LangGraph, LangChain, Google ADK, Python Asyncio + Pydantic v2, Model Context Protocol (MCP), Open WebUI
- **Data, RAG & MLOps Governance:** Qdrant, Apache Tika, MLflow 3.x, Evidently AI, OPA / Kyverno, PostgreSQL, MinIO (S3), Prometheus, Grafana
- **Quantum Computing:** Google Cirq, IBM Qiskit

---

## 📄 License & Contributions

All repositories in **AI Governance Lab** are released under permissive open-source licenses (predominantly **Apache License 2.0**; see individual repository `LICENSE` files). Issues, architectural discussions, and pull requests are welcome.

---

## 👨‍💻 Founder & Lead Maintainer

**Marian Ropota** — *Hands-On AI/ML & Cloud Platform Architect | Hybrid Cloud Infrastructure, LLMOps & Agentic Engineering*  
🔗 **[LinkedIn Profile](https://www.linkedin.com/in/marian-rop)** • 🏅 **[Credly Verified Certifications](https://www.credly.com/users/marian-ropota/badges/credly)** • 🐙 **[AI Governance Lab](https://github.com/AI-Governance-Lab)**