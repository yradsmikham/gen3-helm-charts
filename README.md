# Gen3 Helm Charts

## Prerequisites

1. A kubernetes cluster
2. Helm 3 installed

## Getting Started

### Deploying Postgres (dependency for most Gen3 microservices)

Recommended to use the stable binami postgresql image [here](https://github.com/bitnami/charts/tree/master/bitnami/postgresql/#installing-the-chart).

To deploy postgresl this way, run:

```
$ helm repo add bitnami https://charts.bitnami.com/bitnami
$ helm install postgres -f values.yaml bitnami/postgresql
```
where the `values.yml` can be found in `\postgres\values.yaml` of this repo.


### Deploying Microservice Using Helm

```
cd indexd
helm install indexd .
kubectl get pods
```

## Uninstall Services

```
helm uninstall indexd
helm uninstall postgres
```

## Notes

`helm install indexd . --dry-run` is a good way to have the server render templates and display final kubernetes manifest files.

`kubectl decribe pods` is a good way to show logs for kubenertes pods that are stuck in pending state if `kubectl logs` does not help.
