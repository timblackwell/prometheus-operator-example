# prometheus-operator-example
Playing with prometheus operator

```
kubectl create namespace monitoring
kubectl -n monitoring apply -f prometheus-operator
kubectl -n monitoring apply -f prometheus
kubectl -n monitoring apply -f kube-state-metrics
kubectl apply -f example-app
kubectl -n monitoring port-forward prometheus-prometheus-0 9090:9090
```
