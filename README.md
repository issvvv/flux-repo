# FluxCD

FluxCD is a powerful GitOps tool for automating service deployments in Kubernetes. It monitors the cluster state and synchronizes it with the configuration stored in a Git repository.

> ⚙️ **This repository is my playground for exploring FluxCD.**   
>  Here, I apply various features, test configurations, and practice deployment scenarios.

## Key Features
- Automatic deployment of Kubernetes manifests from Git.
- Configuration management using Helm and Kustomize.
- Container image monitoring and version updates.

## Installation & Setup
1. Install the FluxCD CLI:
    ```bash
    curl -s https://fluxcd.io/install.sh | sudo bash && flux install
    ```
2. Setup application with your preferences:
    ```bash
    flux bootstrap github \
    --owner=$GITHUB_USER \
    --repository=$GITHUB_REPO \
    --branch=main \
    --path=./clusters/minikube \
    --personal
    ```

3. Follow the installation instructions to integrate with your Kubernetes cluster, ensuring authentication with GitHub via PAM.
