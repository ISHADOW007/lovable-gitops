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