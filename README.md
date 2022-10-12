# IDP

This is a test repo for things relating to [ArgoCD](https://argoproj.github.io/cd).

This could have used the Argo AutoPilot project, but this is also an exercise of installing the understanding ArgoCD by building it separately. If this is a production instance or support, please use the [AutoPilot project](https://argocd-autopilot.readthedocs.io/).

## Platform

For local testing [k3d](https://k3d.io/) is used with Rancher Desktop. This runs a k3s cluster in docker. The install method for this is [here](./k3d/argocd/README.md).

## ArgoCD

[ArgoCD](https://argo-cd.readthedocs.io/) is a way of managing deployment in Kubernetes through GitOps.

### Apps

TODO: More to come ...


### Notes

Running Rancher Desktop with its built-in Kubernetes release did not want to enable network comms. If this gets resolved, it should be simple enough to transition to that as they use the `k3` framework.
