# ☸️ GO Helm Chart 

This repository contains a Helm chart for deploying **GOFoods Application**. The chart is packaged and hosted on GitHub Pages for easy installation into Kubernetes cluster.

## ☸️ Chart Details

- **Chart Name**: `gochart`
- **Version**: `0.1.0`
- **Description**: A Helm chart for deploying My Application to Kubernetes.

## ☸️ Prerequisites 👨‍💻

- Kubernetes cluster
- [Helm](https://helm.sh/docs/intro/install/) installed
- `kubectl` configured to interact with Kubernetes cluster

## ☸️ Get to Speed 🚀⚡🚀

To install this Helm chart, add the GitHub repository as a Helm repository:

```bash
minikube start

kubectl config use-context minikube

helm package <path-to-helm-chart>

helm install <release-name> <path-to-helm-chart.tgz>
```

## if using existing chart:
```bash
helm repo add gocharts https://Gad-Ongoro.github.io/helm-charts

helm repo update

helm install server gocharts/gochart
```
