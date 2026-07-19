# 🚀 CI/CD Pipeline Automation Project

## 📌 Overview

A complete **CI/CD pipeline** automating the software lifecycle from commit to deployment and monitoring — covering SCM, CI, testing, code quality, containerization, artifact management, deployment, and observability.

---

## 🏗️ Architecture

![Uploading design (1).gif…]()


Three stages:
1. **Local Dev Workflow** — Developer → Working Dir → Staging → Commit
2. **CI Stage** — GitHub → Jenkins → Build → SonarQube → Nexus → Docker → Docker Hub
3. **CD & Monitoring** — Docker Hub → Deployment Server → Prometheus/Grafana → Alert Manager → Slack

---

## 🔄 Pipeline Flow
![Uploading pipeline.png…]()
---

