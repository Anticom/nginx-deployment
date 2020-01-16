# CFM nginx-ingress deployment

The nginx-ingress is managed via [helm 3](https://helm.sh/).
You can download the latest release of helm client [here](https://github.com/helm/helm/releases).

# Deployment strategy / layout

We decided upon using our own edge service to route traffic into the cluster and deploy nginx-ingress Service as type `NodePort`.