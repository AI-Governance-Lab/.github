# AI-Governance-Lab

Welcome to the **AI Governance Lab** organization! We focus on developing practical tools and demonstrations for AI governance, MLOps, and cloud-native AI deployments.

## About Us

AI-Governance-Lab is dedicated to building solutions that bridge the gap between AI/ML operations and governance requirements. Our projects demonstrate best practices for deploying, monitoring, and managing AI systems in production environments while maintaining compliance with governance frameworks.

## Our Focus Areas

- **AI Governance & Compliance**: Alignment with standards like EU AI Act, NIST AI RMF, ISO/IEC 42001, and GDPR
- **MLOps & LLMOps**: Production-ready ML and LLM deployment patterns
- **Kubernetes-Native AI**: Cloud-agnostic, containerized AI/ML workloads
- **AI Monitoring**: Drift detection, quality assurance, and performance tracking
- **Agentic AI**: RAG systems and AI agent frameworks

## Key Technologies

Our projects leverage modern cloud-native and AI technologies:

- **Orchestration**: Kubernetes (K8s), Helm
- **ML Platforms**: MLflow, Evidently AI
- **LLM Tools**: Ollama, OpenAI, AWS Bedrock
- **Infrastructure**: Terraform, Docker
- **Storage**: MinIO (S3-compatible), PostgreSQL
- **Vector Search**: Qdrant
- **APIs**: FastAPI, Python

## Repositories

### [k8s-mlfow-demo](https://github.com/AI-Governance-Lab/k8s-mlfow-demo)
A minimal production MLflow 3.3.2 stack on k3s using Helm. Features PostgreSQL for tracking, MinIO for artifacts, and NodePort access. LLMOps-ready with guidance for prompts, evaluations, and model registry.

**Topics**: MLflow, MLOps, LLMOps, Kubernetes, Helm, MinIO, RAG, AI Governance

### [k8s-ollama-fastapi-demo](https://github.com/AI-Governance-Lab/k8s-ollama-fastapi-demo)
FastAPI + Ollama LLM demo showcasing containerized AI inference with Kubernetes, ready for governance tools.

**Topics**: Ollama, FastAPI, LLM, Kubernetes, Docker, Agentic AI

### [k8s-ai-agent-multicloud-rag-iac](https://github.com/AI-Governance-Lab/k8s-ai-agent-multicloud-rag-iac)
RAG-powered Kubernetes AI agent for custom-document search and multicloud Infrastructure-as-Code deployments (AWS/Azure/GCP/IBM) with FastAPI, Terraform, and Helm.

**Topics**: AI Agents, RAG, Multicloud, Terraform, AWS EKS, Bedrock, Qdrant, Governance

### [k8s-evidently-demo](https://github.com/AI-Governance-Lab/k8s-evidently-demo)
Kubernetes manifests to run Evidently for drift, quality, and performance monitoring. Features NodePort/port-forward access, optional Ingress and Prometheus/Grafana integration, with alignment to EU AI Act, NIST AI RMF, and ISO/IEC 42001.

**Topics**: Evidently AI, Monitoring, AI Governance, EU AI Act, GDPR, Agentic AI

## Governance Alignment

Our projects are designed with governance in mind, addressing requirements from:

- **EU AI Act**: European Union's regulatory framework for AI
- **NIST AI RMF**: AI Risk Management Framework
- **ISO/IEC 42001**: AI Management System standard
- **GDPR**: General Data Protection Regulation

## Get Involved

We welcome contributions and feedback! Each repository contains detailed documentation on setup, deployment, and usage.

## License

Our projects are released under the Apache License 2.0, promoting open collaboration and innovation in the AI governance space.