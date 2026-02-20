# Production-Ready Kubernetes Deployment on AWS EKS with ALB, SSL and Domain Routing

## Overview

This project demonstrates the design and deployment of a production-style containerized e-commerce application on AWS using Kubernetes (Amazon EKS). The infrastructure and application environment were provisioned using Kubernetes manifests, with external traffic managed through an AWS Application Load Balancer (ALB) integrated with an external domain routing and SSL termination.

The goal of this project was to implement a scalable, secure and reproducible deployment architecture that reflects real-world DevOps and cloud engineering practices.

Live Domain: https://jaychen.co.ke

---

## Architecture

User → Route53 → AWS ALB → Kubernetes Ingress → Services → Pods → Containers

Key components:

- Amazon EKS Cluster (CloudFormation)
- Managed Node Groups
- AWS ALB Ingress Controller
- Containerized application (Docker Hub)
- Kubernetes Deployments and Services
- Route53 DNS configuration
- AWS Certificate Manager (SSL/TLS)
- Path-based routing configuration

---

## Objectives

- Deploy containerized application on Kubernetes
- Provision infrastructure using Infrastructure as Code
- Configure external access via AWS ALB
- Implement domain routing with HTTPS
- Demonstrate production-style DevOps workflow
- Manage application lifecycle on Kubernetes

---

## Infrastructure Provisioning

The Kubernetes cluster and supporting infrastructure were provisioned using AWS CloudFormation templates, including:

- EKS Cluster
- Worker Node Groups
- IAM Roles and Permissions
- ALB Controller service account
- Networking configuration

This approach ensures repeatability and consistency across environments.

---

## Kubernetes Deployment

Application deployment was performed using Kubernetes manifests:

- Namespace configuration
- Deployment resources
- Service exposure
- Ingress configuration
- Load balancer integration

The application container images were pulled from Docker Hub and deployed into the cluster through Kubernetes deployment objects.

---

## Ingress and Load Balancing

The AWS ALB Ingress Controller was configured to:

- Automatically provision an Application Load Balancer
- Route external traffic to Kubernetes services
- Support path-based routing
- Integrate with AWS Certificate Manager for HTTPS

This enabled secure and scalable external access to the application.

---

## Domain and SSL Configuration

The external domain (jaychen.cloud) was configured using AWS Route53.

SSL/TLS certificates were provisioned through AWS Certificate Manager and attached to the ALB, enabling secure HTTPS communication with automatic certificate management.

---

## Technologies Used

- AWS EKS
- AWS CloudFormation
- Kubernetes
- Docker
- AWS ALB Ingress Controller
- AWS Route53
- AWS Certificate Manager
- YAML
- Linux

---

## Key DevOps Practices Demonstrated

- Infrastructure as Code
- Container orchestration
- Cloud-native deployment architecture
- Load balancing and ingress management
- TLS/SSL security implementation
- Domain integration
- Application lifecycle management
- Troubleshooting and verification of cluster components
- Remote-first documentation approach

---

## Challenges and Lessons Learned

Some key challenges encountered included:

- Configuring IAM permissions for ALB controller
- Integrating ingress resources with AWS load balancing
- Debugging Kubernetes networking issues
- Managing DNS propagation and certificate validation
- Verifying pod and service communication across namespaces

These challenges improved understanding of Kubernetes networking, cloud infrastructure integration and deployment troubleshooting.

---

## Screenshots

- EKS Cluster
- <img width="1327" height="616" alt="image" src="https://github.com/user-attachments/assets/52db2e13-2897-4604-b8dc-1157304a14cb" />

- Node Groups
- <img width="1500" height="782" alt="image" src="https://github.com/user-attachments/assets/e74783a0-0140-449c-965e-0aaa9e04b7cd" />

- Cloud Formation Stack
- <img width="1463" height="615" alt="image" src="https://github.com/user-attachments/assets/6a4bb205-482c-4c56-93dd-d13f29eee060" />

- Load Balancer
- Domain with SSL
- Application interface
- <img width="1896" height="925" alt="image" src="https://github.com/user-attachments/assets/4395236d-7872-499f-b747-e892b614563e" />


---

## Future Improvements

- CI/CD pipeline for automated deployments
- Helm-based deployment management
- Monitoring with Prometheus and Grafana
- Auto-scaling configuration
- Blue/Green deployment strategies

---

## Author

James Chege  
DevOps Engineer | Cloud Infrastructure | Kubernetes  

LinkedIn: https://www.linkedin.com/in/jaychen123/
