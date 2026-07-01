# Validation Instructions

## 1. Verify that the application is running
```bash
kubectl get pods
kubectl logs <pod-name>
# or
kubectl port-forward <pod-name> 8080:8080
# Open http://localhost:8080
```

## 2. Verify ConfigMap is mounted as files
```bash
kubectl exec -it <pod-name> -- ls /app/configs
kubectl exec -it <pod-name> -- cat /app/configs/<key-name>
```

## 3. Verify Secret is mounted as file
```bash
kubectl exec -it <pod-name> -- ls /app/secrets
kubectl exec -it <pod-name> -- cat /app/secrets/<secret-key>
```