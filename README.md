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





Great. ✅ Your Spring Boot Micrometer + Actuator + Prometheus + ServiceMonitor integration is fully working.




git add .
git commit -m "My changes"
git pull --rebase origin main
git push origin main



















kubectl get servicemonitor api-gateway -n monitoring -o yaml






kubectl port-forward svc/monitoring-kube-prometheus-prometheus -n monitoring 9090:9090





































Install OWASP CLI once on your Jenkins server

If Jenkins is running in Docker:

docker exec -it jenkins bash

Download the latest release:

cd /opt

wget https://github.com/dependency-check/DependencyCheck/releases/download/v12.2.2/dependency-check-12.2.2-release.zip

apt update
apt install unzip -y

unzip dependency-check-12.2.2-release.zip

ln -s /opt/dependency-check/bin/dependency-check.sh /usr/local/bin/dependency-check

Verify:

dependency-check --version

You should see something like:

Dependency-Check Core version 12.2.2




kubectl apply -f frontend/lovable-frontend/service.yaml
kubectl apply -f frontend/lovable-frontend/deployment.yam

















kubectl create namespace monitoring

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm install monitoring prometheus-community/kube-prometheus-stack --namespace monitoring
kubectl get pods -n monitoring



 kubectl port-forward -n monitoring svc/monitoring-grafana 8086:80
 kubectl get secret monitoring-grafana -n monitoring -o jsonpath="{.data.admin-password}"
 MWvRG2HUeEouwheMjEhfclU11hybhAiVQvp5gg7G




 kubectl get svc -n lovable-core --show-labels
 kubectl get svc api-gateway -n lovable-core -o yaml
  kubectl get deployment api-gateway -n lovable-core --show-labels
   kubectl get deployment account-service -n lovable-core --show-labels
 
 