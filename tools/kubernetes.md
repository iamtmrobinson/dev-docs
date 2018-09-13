# Kubernetes

List available pods:
```
kubectl get pods
```

Create pod from YAML:
```
kubectl apply -f [NAME].yaml
```

Find more info about individual pod:
```
kubectl describe pod [POD_ID]
```

Log into a shell on a pod:
```
kubectl exec -it [POD_ID] -- sh
```