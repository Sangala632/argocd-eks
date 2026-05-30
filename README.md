# argocd-eks

Overview
ArgoCD "app-of-apps" manifests to deploy Roboshop apps into EKS clusters using GitOps.

Why this exists
To enable continuous delivery with declarative manifests tracked in Git and reconciled by ArgoCD.

Workflows
- Update app manifests in this repo
- ArgoCD detects changes and syncs apps to EKS

Actions (quick start)
1. Install ArgoCD on target EKS cluster.
2. Ensure this repo is added as an App of Apps in ArgoCD.
3. Push changes to manifests; monitor ArgoCD UI for sync.

Key files
- app-of-apps.yaml, applications/*, namespaces/*

Notes
- Keep manifests environment-specific via kustomize/overlays.
