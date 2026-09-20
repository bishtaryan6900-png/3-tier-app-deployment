# 🚀 Three-Tier Web Application Deployment on AWS EKS (#TWSThreeTierAppChallenge)

This repository contains the application source code, Docker configurations, and Kubernetes manifests (including Ingress) to deploy a full-stack **Three-Tier Web Application** onto **AWS Elastic Kubernetes Service (AWS EKS)**.

---

## 🛠️ Application Architecture

The application is deployed across three main tiers within the AWS EKS cluster, managed and routed via Kubernetes Ingress:

* **Frontend Tier:** ReactJS application serving the client interface.
* **Backend Tier:** NodeJS REST API executing backend application logic.
* **Database Tier:** MongoDB instance managing persistent data storage.
* **Traffic Routing:** An **Ingress Controller** routes external traffic through an AWS Load Balancer to the respective Frontend and Backend services.

---

## 📁 Repository Structure

```text
.
├── application-code/
│   ├── frontend/           # ReactJS web app
│   └── backend/            # NodeJS API server
└── kubernetes-manifests/
    ├── deploy.yaml         # Kubernetes Deployments (Frontend, Backend, DB)
    ├── svc.yaml            # Kubernetes Services
    ├── secrets.yaml        # Environment variables & DB secrets
    └── ingress.yaml        # Ingress routing rules
