# AI Governance Lab

**Personal Learning Portfolio - AI Governance and Multi-Cloud Deployment Patterns**

Open-source experiments and learning projects exploring secure, compliant, and scalable AI systems across multi-cloud environments. This portfolio documents my journey in understanding enterprise AI deployment, governance, and MLOps practices.

---

## What This Portfolio Demonstrates

**🎯 Learning Objectives**
- Understanding AI deployment patterns and best practices
- Exploring regulatory compliance considerations (GDPR, EU AI Act)
- Hands-on experience with multi-cloud architectures
- Building reproducible, well-documented solutions

**🔧 Technical Skills Demonstrated**
- **Enterprise AI Agents**: Multi-cloud deployment with SAP S/4HANA, IBM watsonx, Google Vertex AI
- **Intelligent Search**: Retrieval-Augmented Generation (RAG) with vector databases
- **ML Operations**: Complete MLOps lifecycle with experiment tracking and model registry
- **Quality Assurance**: Automated drift detection and model performance monitoring
- **Security First**: Secure supply chain, container hardening, least-privilege access

---

## Featured Projects

*Personal learning experiments and open-source contributions*

### 🤖 AI Agent Projects

**[k8s-ai-agent-multicloud-rag-iac](https://github.com/AI-Governance-Lab/k8s-ai-agent-multicloud-rag-iac)** - Multi-Cloud RAG Agent  
Production RAG-powered AI agent with custom document search and Infrastructure-as-Code deployment across AWS, Azure, GCP, and IBM Cloud. Includes FastAPI, Terraform, and Helm charts.  
*Technologies: Kubernetes, Terraform, RAG, Bedrock, OpenAI, Helm*

**[k8s-ai-agents-demo](https://github.com/AI-Governance-Lab/k8s-ai-agents-demo)** - Kubernetes AI Agent Reference  
Reference implementation for containerized AI agent services with Qdrant vector store, FastAPI endpoints, and MLflow integration for tracking.  
*Technologies: Docker, Kubernetes, Qdrant, Watson AI, MLflow*

**[s4hana-ai-agent-openshift](https://github.com/AI-Governance-Lab/s4hana-ai-agent-openshift)** - SAP S/4HANA Automation Agent  
AI-powered automation for SAP S/4HANA deployment on IBM Cloud PowerVS using IBM watsonx.ai, RAG, and Terraform orchestration on Red Hat OpenShift.  
*Technologies: IBM Watson, PowerVS, OpenShift, Terraform, FastAPI, RAG*

### ☁️ Google Cloud / Vertex AI

**[vertex-ai-agentbuilder-demo](https://github.com/AI-Governance-Lab/vertex-ai-agentbuilder-demo)** - Vertex AI Agent Builder  
Complete examples for building intelligent agents using Google's Vertex AI Agent Builder and Agent Development Kit (ADK), including deployment patterns.  
*Technologies: Google Vertex AI, ADK, Agent Engine, Cloud Run*

**[vertex-ai-pipeline-demo](https://github.com/AI-Governance-Lab/vertex-ai-pipeline-demo)** - ML Pipeline Orchestration  
Production MLOps pipelines on Google Cloud using Vertex AI for model training, evaluation, and deployment automation.  
*Technologies: Vertex AI Pipelines, Python, MLOps*

**[vertex-ai-cloudrun-demo](https://github.com/AI-Governance-Lab/vertex-ai-cloudrun-demo)** - Serverless AI Services  
Lightweight Python/Flask microservices exposing Vertex AI embeddings (text-embedding-004) and Gemini LLM via HTTP endpoints on Cloud Run.  
*Technologies: Cloud Run, Gemini, Vertex AI, Docker, Python*

### 📊 ML Experiment Tracking & Model Registry

**[k8s-mlflow-rancher-desktop](https://github.com/AI-Governance-Lab/k8s-mlflow-rancher-desktop)** - Local MLOps Stack  
Developer-laptop stack with MLflow 3.x on Rancher Desktop (k3s), PostgreSQL backend, and MinIO artifact storage for experiment tracking and model registry.  
*Technologies: MLflow, Rancher, k3s, PostgreSQL, MinIO, S3*

**[k8s-mlfow-demo](https://github.com/AI-Governance-Lab/k8s-mlfow-demo)** - Production MLflow Stack  
Production-ready MLflow 3.3.2 deployment on Kubernetes with PostgreSQL tracking store, MinIO artifacts, LLMOps capabilities, and evaluation metrics.  
*Technologies: Kubernetes, MLflow, Helm, MinIO, PostgreSQL, LLMOps*

### 🛡️ Governance & Monitoring

**[k8s-evidently-demo](https://github.com/AI-Governance-Lab/k8s-evidently-demo)** - AI Quality Monitoring  
Kubernetes deployment for Evidently AI to monitor model drift, data quality, and performance. Supports GDPR/EU AI Act compliance with optional Prometheus/Grafana integration.  
*Technologies: Kubernetes, Evidently AI, Prometheus, Governance, EU AI Act*

### 🚀 Model Serving

**[k8s-ollama-fastapi-demo](https://github.com/AI-Governance-Lab/k8s-ollama-fastapi-demo)** - Open-Source LLM Serving  
Containerized AI inference with FastAPI and Ollama for local LLM deployment, ready for integration with governance and monitoring tools.  
*Technologies: FastAPI, Ollama, Kubernetes, Docker, LLM, MLOps*

---




## Core Principles

**🏛️ Governance by Design**  
Built-in auditability, traceability, and compliance controls from the ground up

**🔒 Security & Isolation**  
Container hardening, secure supply chains, and least-privilege access patterns

**🌐 Multi-Cloud Portability**  
Deploy anywhere: AWS, Azure, GCP, IBM Cloud, or on-premises infrastructure

**📈 Observability**  
Comprehensive monitoring for model drift, data quality, and performance degradation

**🧩 Modular Architecture**  
Composable Infrastructure-as-Code and Helm charts for flexible deployment

---

## Getting Started

**For Learners & Contributors:**
1. Browse the [Featured Projects](#featured-projects) above
2. Select a topic that interests you
3. Follow the README documentation for setup and experimentation
4. Fork and adapt for your own learning journey
5. Contributions and feedback welcome!

**Portfolio Purpose:**
- Each project documents my learning process and technical exploration
- All code is Apache 2.0 licensed for educational and personal use
- Experiments based on industry best practices and public documentation
- Shared for community learning and collaboration

---

## Use Cases by Industry

**🏦 Financial Services**  
Compliant AI agents with full audit trails for regulatory requirements

**🏭 Manufacturing & SAP**  
Automated ERP deployments with AI-powered infrastructure orchestration

**🏥 Healthcare & Life Sciences**  
Secure RAG systems for document analysis with GDPR/HIPAA considerations

**☁️ Cloud Service Providers**  
Multi-cloud AI platforms with centralized governance and monitoring

---

## Technology Stack

**Cloud Platforms:** AWS, Azure, GCP, IBM Cloud  
**Orchestration:** Kubernetes, OpenShift, Terraform, Helm  
**AI/ML:** Vertex AI, IBM watsonx, OpenAI, Bedrock, Ollama  
**MLOps:** MLflow, Evidently AI, Prometheus, Grafana  
**Languages:** Python, Docker, FastAPI  
**Vector Stores:** Qdrant  
**Storage:** PostgreSQL, MinIO (S3-compatible)

---

## Portfolio Highlights

✅ **Hands-On Learning**: Real implementations, not just theory  
✅ **Open Source**: Apache 2.0 licensed, transparent and collaborative  
✅ **Multi-Cloud Exploration**: Experience with AWS, Azure, GCP, IBM Cloud  
✅ **Governance Focus**: Understanding compliance and security requirements  
✅ **Continuous Learning**: Ongoing exploration of new technologies  
✅ **End-to-End**: From development to deployment and monitoring

---

## Community & Contributions

**Questions & Discussions:** Open an issue in the relevant repository  
**Contributions Welcome:** PRs appreciated - please include documentation  
**Learning Together:** Share your experiences and improvements

---

## License & Disclaimer

All repositories are licensed under **Apache License 2.0** for educational and personal use.

**Note:** This is a personal learning portfolio showcasing open-source experiments and educational projects. All work is based on publicly available documentation, tutorials, and best practices. Not affiliated with any commercial entity.

---

**Personal Portfolio by Marius Ropota** | Learning through open-source collaboration
