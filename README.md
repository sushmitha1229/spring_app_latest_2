# Spring App on Amazon EKS with CodePipeline

This repo contains:
- `buildspec.yml` → builds Docker image and pushes to ECR
- `appspec.yaml` → defines EKS deployment for CodeDeploy
- `k8s/deployment.yaml` → Kubernetes deployment manifest
- `k8s/service.yaml` → Kubernetes service manifest

### AWS Resources Used
- EKS Cluster: `spring-eks`
- ECR Repo: `263350856766.dkr.ecr.us-east-1.amazonaws.com/spring-app`
- GitHub Repo: `https://github.com/<your-username>/spring_app_latest_2`

### Pipeline Flow
GitHub (Source) → CodeBuild (Build & Push Image) → CodeDeploy (Deploy to EKS)
