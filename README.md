Application-Code

CI/CD Pipeline for Microservices with Jenkins, Docker & Argo CD on EKS
“Designed and implemented a complete CI/CD pipeline for microservices deployment to Amazon EKS using Jenkins, Docker, and Argo CD, following a GitOps workflow with separate source and deployment repositories.”

“This repository demonstrates an end-to-end CI/CD pipeline for building and containerizing microservices using Jenkins and Docker. It uses a separate deployment repository with Argo CD to automatically deploy applications to an Amazon EKS cluster using a GitOps workflow.”

Set up a Jenkins pipeline to build Docker images on every code commit and push them to a container registry such as AWS ECR or Docker Hub.

Organize microservices and Kubernetes manifests in a GitOps-friendly structure using separate repositories.

Configure Argo CD to automatically sync manifests from Git and deploy applications to an Amazon EKS cluster. 🚀

#Pipeline workflow

1.Developer pushes code to the Source Repository. 2.Jenkins CI pipeline triggers, runs SonarQube code analysis, builds the Docker image, and pushes it to AWS ECR. 3.Jenkins updates the Kubernetes deployment.yaml with the new image tag and commits the change to the Deployment Repository. 4.Argo CD detects the update, syncs the manifests, and deploys the application to Amazon EKS.

**Final Architecture**

Developer

   ↓
   
GitHub (Source Repo)

   ↓
   
Jenkins Pipeline

   ↓
   
Docker Build

   ↓
   
AWS ECR

   ↓
   
Update Deployment Repo

   ↓
   
ArgoCD (GitOps)

   ↓
   
Kubernetes (EKS)

   ↓
   
LoadBalancer

   ↓
   
Browser → HTML Website

5.The application becomes live on Kubernetes.
