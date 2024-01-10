# kubernetes
## Pod template resources limit/request needs to be set
apiVersion: v1
kind: Pod
metadata:
  name: cpu-demo
  namespace: cpu-example
spec:
  containers:
  - name: cpu-demo-ctr
    image: vish/stress
    resources:
      limits:
        cpu: "1"
      requests:
        cpu: "0.5"
    args:
    - -cpus
    - "2" 


## Helm search repo / metrics-server
```
helm repo add metrics-server https://kubernetes-sigs.github.io/metrics-server/
```

## Helm install metrics-server
```
helm upgrade --install metrics-server metrics-server/metrics-server
```
