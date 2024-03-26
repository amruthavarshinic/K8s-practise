# K8s-practise

### Pods:
```sh
# Create nginx pod defination/manifest file
kubectl run nginx --image=nginx --dry-run=client -o yaml > nginx.yaml

# Create nginx pod with kubectl CMD
kubectl run nginx --image=nginx

# Create nginx pod with pod defination/manifest file
kubectl create -f nginx.yaml
           (OR)
kubectl apply -f nginx.yaml

# List all pods
kubectl get pods -A

# List pods in default namespace
kubectl get pods -n default

# Describe pod
kubectl describe pod <pod name> -n <namespace>

# Check logs 
kubectl logs -f <pod name> -n <namespace>

# Edit pod
kubectl edit pod <pod name> -n <namespace>

# Delete pod 
kubectl delete pod <pod name> -n <namespace> --force --grace-period=0
```