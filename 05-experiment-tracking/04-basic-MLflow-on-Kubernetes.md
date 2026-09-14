Please refer to the below documentation for this lecture.

https://community-charts.github.io/docs/charts/mlflow/basic-installation - Please follow the below steps, i didn't followed this doc

```bash
kind create cluster --name=basic-mlflow-cluster

helm repo add community-charts https://community-charts.github.io/helm-charts
helm repo update community-charts

helm install mlflow-community community-charts/mlflow

kubectl get pods --> mlflow pod should be in running state
kubectl port-forward pod/mlflow-community-6d575f4f6b-28cxb 7006:5000 --address 0.0.0.0  -> try to access it

# uninstall it
helm uninstall mlflow-community
```

