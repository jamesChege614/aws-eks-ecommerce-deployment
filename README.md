# Production-Ready Kubernetes Deployment on AWS EKS with ALB, SSL and Domain Routing

## Overview

This project demonstrates the design and deployment of a production-style containerized e-commerce application on AWS using Kubernetes (Amazon EKS). The infrastructure and application environment were provisioned using Infrastructure as Code and Kubernetes manifests, with external traffic managed through an AWS Application Load Balancer (ALB) integrated with domain routing and SSL termination.

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

The external domain (jaychen.co.ke) was configured using AWS Route53.

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

(Add screenshots here)

- EKS Cluster
- Node Groups
- Running Pods
- Load Balancer
- Domain with SSL
- Application interface

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
