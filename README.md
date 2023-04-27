# argo-cd

### Getting Started

Pre-reuisites - Docker, K8s cluster

1. Install Argo CD (using UI)
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

2. Download latest version (ArgoCD CLI)
```
curl -sSL -o argocd-linux-amd64 https://github.com/argoproj/argo-cd/releases/latest/download/argocd-linux-amd64
sudo install -m 555 argocd-linux-amd64 /usr/local/bin/argocd
rm argocd-linux-amd64
```

3. Access The Argo CD API Server
```
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
```

Port Forwarding
```
kubectl port-forward svc/argocd-server -n argocd 8080:443
```
