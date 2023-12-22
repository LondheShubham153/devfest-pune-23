# DevFest Pune 23 - Kubernetes Autopilot and Google Cloud Shell

Welcome to the DevFest Pune 23 GitHub repository! This repository contains instructions and resources to help you get started with Google Kubernetes Engine (GKE) Autopilot and Google Cloud Shell. 

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [Install HELM](#install-helm)
  - [Install nginx-controller](#install-nginx-controller)
- [Kubernetes Autopilot](#kubernetes-autopilot)
  - [Create a Namespace](#create-a-namespace)
  - [Deploy an Application](#deploy-an-application)
- [Google Cloud Shell](#google-cloud-shell)
- [Useful Commands](#useful-commands)

## Introduction
This repository provides a step-by-step guide to setting up a Kubernetes environment with GKE Autopilot and using Google Cloud Shell for management and deployment tasks.

## Prerequisites
Before you begin, make sure you have the following prerequisites:
- A Google Cloud Platform (GCP) account with billing enabled.
- Google Cloud SDK (gcloud) installed on your local machine.
- Access to a GKE cluster with Autopilot enabled.


# Google Cloud Shell
Google Cloud Shell provides a browser-based shell environment that you can use for managing your GCP resources and interacting with Kubernetes clusters.

To access Google Cloud Shell, follow these steps:

Log in to your GCP Console.
Click on the "Activate Cloud Shell" button in the upper-right corner.

### Install HELM
To install HELM, use the following commands:

```bash
# Add the HELM repository
helm repo add helm https://helm.sh/helm
# Update the repository
helm repo update
# Install nginx-controller
To install the nginx-controller, use the following commands:
```
```bash
Copy code
# Add the nginx-controller repository
helm repo add nginx https://kubernetes.github.io/ingress-nginx
# Update the nginx-controller repository
helm repo update
# Search for the nginx-controller chart
helm search repo nginx
```

# On Shell
## Create a Namespace
You can create a Kubernetes namespace using the following command:

``` bash
kubectl create namespace <namespace-name>
# Deploy an Application

To deploy an application, apply the YAML configuration file to your namespace:
```
```bash

kubectl apply -f <path-to-yaml-file>
```

# Useful Commands
Here are some useful commands to help you manage your Kubernetes environment:

``` bash

# List all ValidatingWebhookConfigurations in all namespaces
kubectl get ValidatingWebhookConfiguration -A

# Delete a ValidatingWebhookConfiguration (e.g., nginx-ingress-nginx-admission)
kubectl delete -A ValidatingWebhookConfiguration nginx-ingress-nginx-admission

# List all pods in the current namespace
kubectl get pods

# Create a new Kubernetes namespace (e.g., "dev" or "sit")
kubectl create ns <namespace-name>

# Apply a YAML configuration file to create resources
kubectl apply -f <path-to-yaml-file>
```

If you have any questions or encounter issues, please don't hesitate to open an issue or reach out to the community for assistance.

Happy learning at DevFest Pune 23! 🚀