# CFM nginx-ingress deployment

The nginx-ingress is managed via [helm 3](https://helm.sh/).
You can download the latest release of helm client [here](https://github.com/helm/helm/releases).

# Deployment strategy / layout

We decided upon using our own edge service to route traffic into the cluster and deploy nginx-ingress Service as type `NodePort`.

# FAQ:

## How do I get the original values file using helm 3?
```bash
$ helm show values stable/nginx-ingress
#                  ^
#                  name of the chart
```

## How to I inspect what the final deployment objects will look like given my `values.yaml`
```bash
$ helm template -f values.yaml nginx-ingress stable/nginx-ingress
#                                            ^
#                              ^             name of the chart
#                              release name (the name the chart will be installed as to uniquely identify the installation)
```