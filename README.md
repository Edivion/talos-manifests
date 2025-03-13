# Manifests for Talos Linux

This repository contains ready-to-deploy Kubernetes manifests designed specifically for use with Talos Linux installations. These manifests are intended to simplify the process of configuring and deploying essential services on a Talos-based Kubernetes cluster.

... work in progress ;)

## CNI / Antrea
```shell
## manual Antrea helm install
helm repo add antrea https://charts.antrea.io
helm repo update
helm install -n kube-system antrea -f cni/values.yml antrea/antrea``
# generate a new manifest:
helm template -n kube-system antrea -f cni/values.yaml antrea/antrea > cni/antrea.yaml
```
