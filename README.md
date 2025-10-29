# Ingress Demo on Minikube

This repository demonstrates how to set up and test **Kubernetes Ingress** locally using **Minikube**.  
It includes a simple deployment, service, and ingress configuration to expose an application via an NGINX ingress controller.

## Prerequisites

- Docker Desktop or VirtualBox
- Minikube
- kubectl
- Git

## Setup Steps

1. **Start Minikube**
     minikube start
     Enable Ingress Addon

2. minikube addons enable ingress
# This installs nginx ingress controller on minikube
3. Deploy the Sample App
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
    kubectl apply -f ingress.yaml
4. Verify Resources
    kubectl get pods
    kubectl get svc
    kubectl get ingress
5. Access the App
    Add the Minikube IP and hostname to your hosts file:
    <minikube-ip>  example.local

6. curl http://example.local
