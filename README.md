# Kubernetes

Quickly setup a Kubernetes cluster in various environments

|  Cluster         | Folder                            |
|  ------          | -----                             |
|   `minikube`     | [minikube/](minikube/)            |  
|   `kind`         | [kind/](kind/)                    |

## Minikube

More information available [here](https://minikube.sigs.k8s.io/docs/start/)

```bash
cd minikube
make minikube   
```

By default it creates a cluster with the following parameters:

```bash
minikube start \
    --driver virtualbox \
    --kubernetes-version v1.19.4 \
    --cni cilium \
    --memory 2048 \
    --cpus 2
```

You can change any of the parameters setting the appropriate variable:

```bash
# Change version to 1.20.2
make minikube kubernetes-version=v1.20.2

# Change version to 1.18.14
make minikube kubernetes-version=1.18.14

# Increase memory and cpu
make minikube memory=4096 cpu=4
```

Enable addons via:

```bash
make addons
# enables ingress and metrics servers add-ons
```

Clean up:

```bash
make delete
```

## Kind

More information available [here](https://kind.sigs.k8s.io/docs/user/quick-start/)

```bash
cd kind
make kind
```
