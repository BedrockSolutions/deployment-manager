# Google Kubernetes Engine (GKE)

This template creates a Google Kubernetes Engine cluster.

## Prerequisites

- Install [gcloud](https://cloud.google.com/sdk)
- Create a [GCP project, set up billing, enable requisite APIs](../project/README.md)
- Create a [network and subnetwork](../network/README.md)
- Grant the [container.admin](https://cloud.google.com/kubernetes-engine/docs/how-to/iam) IAM role to the Deployment Manager service account

## Deployment

### Resources

- [container-v1beta1:projects.locations.clusters](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1beta1/projects.locations.clusters)
- [container.v1.cluster](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters)

### Properties

See the `properties` section in the schema file(s):

- [GKE cluster schema](gke.py.schema)

### Usage

Create your deployment as described below, replacing <YOUR_DEPLOYMENT_NAME> with your with your own deployment name

```shell
    gcloud deployment-manager deployments create <YOUR_DEPLOYMENT_NAME> \
        --config testnet.yaml
```

In case you need to delete your deployment:

```shell
    gcloud deployment-manager deployments delete <YOUR_DEPLOYMENT_NAME>
```
