# Cosmocloud-Deploy

Cosmocloud-Deploy is a Kubernetes-based deployment for a sample web application consisting of a backend, frontend, and Redis for caching. This project uses Helm charts to package and deploy the application into a Kubernetes cluster. The frontend and backend are exposed via services, and Redis is used as a caching service.

## Project Structure

- **templates/**: Contains the Kubernetes manifests such as deployments, services, and other resources required to deploy the application.
- **Chart.yaml**: The metadata for the Helm chart.
- **values.yaml**: The values file for configuring the Helm chart.
- **README.md**: This file with instructions and information about the project.

## Prerequisites

Before you start, ensure you have the following tools installed:

1. **Kubernetes Cluster**: A Kubernetes cluster should be running, which can be accessed using `kubectl`.
2. **Helm**: A package manager for Kubernetes, required to deploy the Helm chart. You can install Helm from [here](https://helm.sh/docs/intro/install/).
3. **kubectl**: To interact with the Kubernetes cluster, you need `kubectl` installed. You can install it from [here](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

## Setup Steps

### 1. Clone the Repository

Clone the `cosmocloud-deploy` repository to your local machine.
###bash
git clone https://github.com/manoj-2003/cosmocloud-deploy.git
cd cosmocloud-deploy

###2.Verify the project Structure 
cosmocloud-deploy/
├── templates/
├── Chart.yaml
├── values.yaml
└── README.md
3.Lint Helm Chart
```bash ```
```helm lint cosmocloud-deploy```
4.Install Helm Chart
```bash```
```helm install testapp cosmocloud-deploy --atomic --timeout 30s```

5.Check Deployment Status
```bash
kubectl get all







