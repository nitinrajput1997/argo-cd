# argo-cd

### Getting Started

Pre-reuisites - Docker, K8s cluster

1. Install Argo CD
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```
