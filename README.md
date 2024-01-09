# kubernetes
## Helm search repo / metrics-server
```
helm repo add metrics-server https://kubernetes-sigs.github.io/metrics-server/
```

## Helm install metrics-server
```
helm upgrade --install metrics-server metrics-server/metrics-server
```
