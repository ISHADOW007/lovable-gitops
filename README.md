# Lovable GitOps Repository

This repository contains the Kubernetes manifests for the Lovable Microservices platform.

## Architecture

Application Repository
↓

Jenkins CI

↓

DockerHub

↓

GitOps Repository (this repository)

↓

ArgoCD

↓

Kubernetes

## Components

- Backend Microservices
- Frontend
- Infrastructure
- ArgoCD Applications

## Deployment

ArgoCD continuously watches this repository.

Any change to Kubernetes manifests will automatically be synchronized to the Kubernetes cluster.





kubectl apply -f argocd\backend.yaml
kubectl get applications -n argocd
kubectl apply -f argocd\infrastructure.yaml


kubectl get application lovable-backend -n argocd -o yaml

kubectl kustomize backend




kubectl apply -f argocd\backend.yaml