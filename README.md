# PLG Stack - Prometheus, Loki, Grafana on Kubernetes

This repository contains Kubernetes configuration files and setup instructions for deploying and configuring the PLG stack, which consists of Prometheus, Loki, and Grafana. This stack is used for monitoring and log aggregation in a Kubernetes cluster.

## Table of Contents

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Getting Started](#getting-started)
   - [Prometheus](#prometheus)
   - [Loki](#loki)
   - [Grafana](#grafana)
4. [Customization](#customization)
5. [Contributing](#contributing)
6. [License](#license)

## Introduction

The PLG stack is a popular combination of open-source tools for monitoring and log management:
![image](https://github.com/infinite8loop/PLG-Prometheus-Loki-Grafana-Stack/assets/103845823/6dcf20c1-33dd-45db-aacb-c585ab622531)

- **Prometheus**: An open-source monitoring and alerting toolkit.
- **Loki**: A horizontally-scalable, highly-available, multi-tenant log aggregation system.
- **Grafana**: A popular open-source platform for monitoring and observability.

This repository provides Kubernetes configuration files (YAML) and instructions for setting up these tools in a Kubernetes cluster.

## Prerequisites

Before getting started, ensure that you have the following prerequisites:

- Access to a Kubernetes cluster.
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) CLI tool installed and configured to interact with your cluster.
- [Helm](https://helm.sh/docs/intro/install/) (optional, for Helm-based installations).
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) (for cloning this repository).

## Getting Started

Follow the instructions below to set up the PLG stack on your Kubernetes cluster.

### Prometheus

1. Navigate to the `prometheus` folder.

2. Edit the `prometheus.yaml` file to customize your Prometheus configuration.

3. Deploy Prometheus using `kubectl`:

   ```bash
   kubectl apply -f prometheus/
Prometheus will be deployed in your cluster.
## Loki
Navigate to the loki folder.

Edit the loki.yaml file to customize your Loki configuration.

Deploy Loki using kubectl:

bash
kubectl apply -f loki/
Loki will be deployed in your cluster.

## Grafana
Navigate to the grafana folder.

Edit the grafana.yaml file to customize your Grafana configuration.

Deploy Grafana using kubectl:

bash
kubectl apply -f grafana/
Grafana will be deployed in your cluster. You can access it via a NodePort or use an ingress controller to expose it externally.

## Deploy sample app along with Fluentbit as sidecar using kubectl:

bash
kubectl apply -f fluentbit-sidecar/
sample app along with Fluentbit will be deployed in your cluster. You can access it via a NodePort or use an ingress controller to expose it externally.

Logs are streamed to Grafana:
![image](https://github.com/infinite8loop/PLG-Prometheus-Loki-Grafana-Stack/assets/103845823/8289eeff-f668-4131-811a-62dda9dc8304)

Customization
You can customize each component's configuration by editing the respective YAML files. Additionally, you can add your own dashboards and alerts to Grafana to monitor your specific services and applications.
