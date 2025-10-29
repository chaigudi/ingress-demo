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
2. **Enable Ingress Addon**
        minikube addons enable ingress
4. **Deploy the Sample App**
    kubectl apply -f deployment.yaml;
    kubectl apply -f service.yaml;
    kubectl apply -f ingress.yaml;
5. **Verify Resources**
    kubectl get pods;
    kubectl get svc;
    kubectl get ingress;
6. **Add the Minikube IP and hostname to your hosts file:**
    <minikube-ip>  example.local
7. **Access the App**
     curl http://example.local
