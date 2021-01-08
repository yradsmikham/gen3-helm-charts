# Gen3 Helm Charts

## Prerequisites

1. A kubernetes cluster
2. Helm 3 installed

## Getting Started
```
cd indexd
helm install indexd .
kubectl get pods
```

## Notes

`helm install indexd . --dry-run` is a good way to have the server render templates and display final kubernetes manifest files.

`kubectl decribe pods` is a good way to show logs for kubenertes pods that are stuck in pending state if `kubectl logs` does not help.
