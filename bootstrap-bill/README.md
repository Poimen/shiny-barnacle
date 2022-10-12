# Kubernetes environment bootstrapping

## k3d for k3s

The `k3d` environment was created using:

> k3d cluster create -p "9090:80@loadbalancer"

The `nginx-test` folder can used to see that the ingress for the k3d cluster is working correctly.

## k3s for wsl2

TODO ... sounds like fun, need to try it