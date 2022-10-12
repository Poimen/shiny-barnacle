# ArgoCD Notes

** NOTE ** : For production systems, use [AutoPilot](https://argocd-autopilot.readthedocs.io)

## Installation

The installation uses Kustomize to run ArgoCD behind Traefik on k3d.

> kubectl apply -k installation

Wait for all the pods to go into the "Running" state.

This will configure ArgoCD UI on the route [/argocd](http://argocd.internal:9090)

In the `host` file, the `argocd.internal` is mapped to `127.0.0.1`.

Attempted to use `argocd.local.gd`, but this fails to login...

The default install password can be found by running:
> kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo

(same as the [Getting Started Guide](https://argo-cd.readthedocs.io/en/stable/getting_started/))

## Uninstall

> kubectl delete -k installation
