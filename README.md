# Homelab K8s Apps

This repository contains the configuration for a Kubernetes-based homelab, managed with Helm and Helmfile.

## Applications

This repository deploys the following applications:

*   **Ingress-Nginx:** An Ingress controller for Kubernetes using NGINX as a reverse proxy and load balancer.
*   **Longhorn:** A distributed block storage system for Kubernetes.
*   **Jenkins:** An open-source automation server for building, testing, and deploying software.
*   **Harbor:** An open-source registry for storing, signing, and scanning container images.
*   **MetalLB:** A load-balancer implementation for bare metal Kubernetes clusters.
*   **Minio:** A high-performance, S3 compatible object storage.

## Structure

The repository is structured as follows:

*   `helmfile.yaml`: The main Helmfile configuration, which defines the Helm releases to be deployed.
*   `manifests/`: Contains raw Kubernetes manifests for applications not managed by Helm.
    *   `metallb/`: Configuration for MetalLB.
    *   `minio/`: Configuration for Minio.
*   `values/`: Contains `values.yaml` files for the Helm charts, allowing for customization of the deployments.
    *   `harbor/`: Harbor values.
    *   `ingress-nginx/`: Ingress-Nginx values.
    *   `jenkins/`: Jenkins values.
    *   `longhorn/`: Longhorn values.

## Usage

To deploy the applications in this repository, you will need to have [Helm](https://helm.sh/) and [Helmfile](https://github.com/helmfile/helmfile) installed.

Then, you can run the following command:

```bash
helmfile apply
```
