# Grafana-Sitecore Demo

This repository contains Kubernetes configurations for running Sitecore with Grafana monitoring stack.

## Components

- Grafana for visualization and monitoring
- Sitecore Content Management (CM)
- Sitecore Content Delivery (CD)
- Sitecore Identity Server (ID)
- Loki for log aggregation
- Prometheus for metrics collection
- Redis for session management
- Solr for search functionality

## Prerequisites

- Kubernetes cluster with both Windows and Linux nodes
- kubectl configured with cluster access
- Docker registry access for Sitecore images
- Required secrets configured in Kubernetes

## Deployment

1. Create required secrets (see Secrets section below)
2. Apply the Kubernetes configurations:
   ```bash
   kubectl apply -k .
   ```

## Secrets

The following secrets need to be configured in your Kubernetes cluster:
- sitecore-database
- sitecore-identity
- sitecore-telerik
- sitecore-license
- sitecore-log-level
- sitecore-solr
- sitecore-graphql
- sitecore-protect-media-requests
- sitecore-docker-registry

Note: Secret values are not included in this repository and need to be configured separately.

## Architecture

- CM and CD services run on Windows nodes
- Monitoring stack (Grafana, Loki, Prometheus) runs on Linux nodes
- Services are exposed through Kubernetes services
- Persistent storage is used for logs and configurations

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

[Add your license information here] 