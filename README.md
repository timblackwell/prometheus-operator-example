# prometheus-operator-example
Playing with prometheus operator

To monitor cluster:
```
kubectl create namespace monitoring
kubectl -n monitoring apply -f prometheus-operator
kubectl -n monitoring apply -f prometheus
kubectl -n monitoring apply -f kube-state-metrics
kubectl -n monitoring apply -f node-exporter
kubectl -n monitoring port-forward prometheus-prometheus-0 9090:9090
```

Example application monitoring:
```
kubectl apply -f example-app
```
