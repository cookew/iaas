# About

This is a mirror of my of git repository I use with [ArgoCD](https://argoproj.github.io/cd/) for deploying my [OKD](https://okd.io/) [Kubernetes](https://kubernetes.io/) cluster at home.

# Deploy

1. Apply your sealed secret cluster keys to the kube-system namespace
2. Update sealed secrets for Argo and cert-manager if needed
3. kustomize build --enable-helm | oc apply -f -

# Sealed Secrets

Sealed secrets are used for the cert-manager cluster ca cert and key, and for the Argo SSH key. The sealed secrets should be placed in those app's sealed secret directory.

* /apps/argo/sealedsecrets
* /apps/cert-manager-certs/sealed-secrets
