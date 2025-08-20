# Kubernetes Configuration Files

This repository contains Kubernetes configuration examples and learning materials.

## Structure

```
k8s-stuff/
├── pods/           # Pod definitions
├── deployments/    # Deployment definitions
├── replicasets/    # ReplicaSet definitions
└── README.md
```

## Contents

### Pods
- `pods/def-pod.yaml` - Basic nginx pod definition
- `pods/nginx-pod.yaml` - Generated nginx pod (kubectl output)
- `pods/nginx-pod.json` - Same pod definition in JSON format

### Deployments
- `deployments/def-deploy.yaml` - Clean nginx deployment with 3 replicas
- `deployments/nginx-deploy.yaml` - Generated deployment (kubectl output)

### ReplicaSets
- `replicasets/redis-rs.yaml` - Frontend ReplicaSet example using Redis

## Usage

### Prerequisites
- Kubernetes cluster (minikube, kind, or cloud provider)
- kubectl configured

### Applying Configurations

**Create a pod:**
```bash
kubectl apply -f pods/def-pod.yaml
```

**Create a deployment:**
```bash
kubectl apply -f deployments/def-deploy.yaml
```

**Create a replicaset:**
```bash
kubectl apply -f replicasets/redis-rs.yaml
```

### Useful Commands

```bash
# View pods
kubectl get pods

# View deployments
kubectl get deployments

# View replicasets
kubectl get replicasets

# Delete resources
kubectl delete -f <filename>
```

## Notes

- All configurations use standard Kubernetes API versions
- Examples are designed for learning and testing purposes
- Remember to clean up resources when done: `kubectl delete -f <filename>`
