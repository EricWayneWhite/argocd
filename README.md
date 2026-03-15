# argocd
Repo to manage ArgoCD

```bash
kubectl apply -k cluster-config -n kube-system
kubectl apply -k cert-manager -n cert-manager
kubectl apply -k argocd -n argocd --server-side --force-conflicts
// If the apply for argocd fails, run it again. It might fail the first time due to missing CRDs

// Before applying the Applications, you might need to update the repoURL and targetRevision
// if you are working on custom branch
kubectl apply -k argo-root -n argocd
```
