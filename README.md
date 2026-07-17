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


kubectl apply -f infrastructure\namespace\namespace.yaml
kubectl apply -f infrastructure\namespace
kubectl apply -f stateful\

kubectl get applications -n argocd

kubectl create secret generic app-secrets --from-env-file=.env -n lovable-previews
kubectl create secret generic app-secrets --from-env-file=.env -n lovable-core
kubectl apply -f argocd\backend.yaml


kubectl port-forward svc/argocd-server -n argocd 8087:443







kubectl apply -f argocd/infrastructure.yaml
kubectl apply -f argocd/stateful.yaml
kubectl apply -f argocd/backend.yaml
kubectl apply -f argocd/frontend.yaml


kubectl get applications -n argocd



kubectl describe application lovable-infrastructure -n argocd
kubectl describe application lovable-stateful -n argocd
kubectl describe application lovable-backend -n argocd
kubectl describe application lovable-frontend -n argocd