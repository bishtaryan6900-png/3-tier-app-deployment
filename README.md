
# 🚀 Three-Tier Web Application Deployment on AWS EKS 

![Project Architecture](architecture.png)

This repository contains the source code, Docker configurations, and Kubernetes deployment manifests for a full-stack **Three-Tier Web Application** built with ReactJS, NodeJS, and MongoDB[cite: 6]. The application is containerized with Docker, pushed to Amazon Elastic Container Registry (ECR), and deployed onto AWS Elastic Kubernetes Service (EKS) with Ingress traffic routing[cite: 6, 7].

---

## 🛠️ Application & Infrastructure Architecture

1. **Containerization:** Each application tier (ReactJS frontend, NodeJS backend, MongoDB database) is containerized using Docker[cite: 6, 7].
2. **Container Registry (Amazon ECR):** The built Docker images for Frontend and Backend are pushed to **Amazon ECR**[cite: 6, 7].
3. **Orchestration (AWS EKS):** The containers are pulled from ECR and deployed into **Kubernetes Pods** within an AWS EKS Cluster[cite: 6, 7].
4. **Traffic Management (Ingress):** Incoming user traffic is routed through an **Ingress / Load Balancer** to direct requests to the appropriate Kubernetes Pods[cite: 6, 7].

---

## 📁 Repository Structure

```text
.
├── application-code/
│   ├── frontend/           # ReactJS source code & Dockerfile
│   └── backend/            # NodeJS API source code & Dockerfile
└── kubernetes-manifests/
    ├── deploy.yaml         # Kubernetes Deployments (Frontend, Backend, MongoDB)
    ├── svc.yaml            # ClusterIP & LoadBalancer Services
    └── ingress.yaml        # Ingress routing configuration
