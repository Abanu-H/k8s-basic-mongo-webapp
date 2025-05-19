### Kubernetes MongoDB + WebApp Demo
A simple Kubernetes application setup using Minikube. This project deploys a Node.js web app connected to a MongoDB backend. It includes YAML manifests for Pods, Services, Secrets, and ConfigMaps — making it ideal for learning basic Kubernetes deployment patterns.

This project contains a basic Kubernetes setup using Minikube that deploys:

- A MongoDB instance with secrets
- A simple web app connected to MongoDB
- Exposed via NodePort for external access

## 🧱 Components

| File | Description |
|------|-------------|
| `mongo-secret.yaml` | Kubernetes secret for MongoDB credentials |
| `mongo-configmap.yaml` | ConfigMap for MongoDB service name |
| `mongo-deployment.yaml` | MongoDB deployment and service |
| `webapp-deployment.yaml` | Webapp deployment and service |
| `README.md` | Project overview |

## 🛠 Requirements

- Minikube
- kubectl
- Docker (optional for building images)

## 🚀 Getting Started

```bash
# Start Minikube
minikube start

# Apply the configurations
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo-configmap.yaml
kubectl apply -f mongo-deployment.yaml
kubectl apply -f webapp-deployment.yaml

# Get Minikube IP
minikube ip -o wide

# Minikube Port Forwarding / Use Minikube to tunnel the service:
minikube service webapp-service
This will open the browser with the URL (usually something like http://127.0.0.1:<PORT>).




