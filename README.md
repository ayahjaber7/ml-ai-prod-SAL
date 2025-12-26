# Cloud-Native Movie Recommender – Team SAL  

**Course:** ML & AI in Production  

---

## Team Information

**Team Name:** Team SAL  
**GitHub Repo:** [https://github.com/ayahjaber7/ml-ai-prod-SLA](https://github.com/ayahjaber7/ml-ai-prod-SLA)

| Name | Role | Focus Area | Summary |
|------|------|-------------|----------|
| **Ayah Jaber** | PM / Delivery Lead & DevOps Lead (Backup ML Lead) | CI/CD, Cloud Deploy, SRE | B.S. in Computer Science (Cybersecurity & AI minors), M.S. in AI in progress. Software QA Engineer in healthcare tech. Interested in AI for humanitarian aid. |
| **Saika Zaman** | ML Lead (Backup Data/Streaming & DevOps) | Modeling & Evaluation | B.S. and M.S. in Computer Science; Ph.D. candidate in AI/ML. Research focus on Federated Learning and Machine Intelligence. |
| **Lawrence Egharevba** | Data/Streaming Lead (Backup PM & DevOps) | Kafka / ETL Pipelines | B.S. in Computer Engineering, M.S. in AI in progress. Interested in scalable AI and ML applications across domains. |

---

## Project Overview

This project implements a **cloud-native movie recommendation system** using the **MovieLens dataset** and **Kafka streaming** for real-time personalization.  
The model employs **collaborative filtering (KNN, SVD)** to predict user–item preferences and serves recommendations through a **FastAPI microservice** deployed on **Google Cloud Run**.

**Goal:** Deliver real-time, scalable, and monitored recommendations that maintain reliability, low latency, and data consistency.

**Service-Level Objectives (SLOs):**
- **Latency (p95):** ≤ 400 ms  
- **Uptime:** ≥ 99.5 %  
- **Accuracy:** ≥ baseline F1 score  

---

## Architecture Summary

**Core Components:**
- **FastAPI Service** – Serves `/recommend`, `/healthz`, and `/metrics` endpoints.  
- **Kafka Topics** – Handle user activity and rating streams.  
- **Schema Registry** – Maintains data schema consistency.  
- **Model Service** – Generates predictions using stored model versions.  
- **GCS Storage** – Persists datasets, model artifacts, and logs.  
- **CI/CD Pipeline** – GitHub Actions for test → build → push → deploy.  
- **Monitoring Stack** – Prometheus + Grafana Cloud dashboards.  

![System Architecture Diagram](docs/architecture_diagram.png)


Figure 1 – System Architecture Diagram

---

## Repository Hygiene Notes
- `.gitignore` excludes environment files, logs, caches  
- `requirements.txt` includes pinned package versions  
- CI/CD pipeline configured for automated deploys  
- Secrets managed via GitHub Environments and Google Secret Manager  

---

**Maintained by:** Team SAL (2025 Fall – ML & AI in Production FAU)
