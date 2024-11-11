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

kubectl create secret generic go-secrets --from-env-file=gofoods.env

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/cloud/deploy.yaml

helm package <path-to-helm-chart>

helm install <release-name> <path-to-helm-chart.tgz>
```

## if using existing chart:
```bash
helm repo add gocharts https://Gad-Ongoro.github.io/helm-charts

helm repo update

helm install server gocharts/gochart
```

## CI/CD act Test
```bash
export SSH_PRIVATE_KEY=$(cat ~/.ssh/id_rsa)

export HELM_TOKEN=(access_token)

act -s HELM_TOKEN -s SSH_PRIVATE_KEY
```

if error dial unix /var/run/docker.sock: connect: permission denied:
```bash
$ which act

>_ output/.../act

$ sudo output /.../act -s HELM_TOKEN -s SSH_PRIVATE_KEY
```
