# Projeto Devops Bare-metal

Projeto de criação de um cluster Kubernetes local para estudos.

## Tecnologias utilizadas

- Kind
- Metallb
- ArgoCD
- Ingress Controller
- Goldilock

## ArgoCD
_Procedimento de instalação:

###Criar namespace argocd

```kubectl create namespace argocd```

###Instalação como operador no Kubernetes

```
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

###Instalar ArgoCD CLI

```
curl -sSL -o argocd-linux-amd64 https://github.com/argoproj/argo-cd/releases/latest/download/argocd-linux-amd64

sudo install -m 555 argocd-linux-amd64 /usr/local/bin/argocd

rm argocd-linux-amd64
```
###Aplicar manifesto Argocd

```
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```