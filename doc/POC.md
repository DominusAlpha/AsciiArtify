# Instruction for get access to the ArgoCD UI
---
## Prerequisites

ArgoCD up and running in cluster

---

## Run commands below

### Get the initial password  

    kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo

### Set port forwarding to the localhost

    kubectl port-forward svc/argocd-server -n argocd 8080:443

---

## Go to the localhost https://127.0.0.1:8080

---
## Login to the ArgoCD as Admin with the initial password

---

[login](data/argoLogin.gif)