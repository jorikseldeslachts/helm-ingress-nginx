# helm-ingress-nginx

## About
Customized version of ingress-nginx Kubernetes ingress controller.
This project will provide helm charts for current and future versions of the ingress controller.
It is meant to be used by my Kubernetes-Ansible project.


## Install Helm 3
Install `Helm 3` on your machine using the instructions on [helm.sh](https://helm.sh/docs/intro/install/).
```sh
# download and install helm binary
$ curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
$ chmod 700 get_helm.sh
$ ./get_helm.sh
```


## Setup
```sh
# add the helm repo
$ helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx

# check repo
$ helm repo list

# install the helm chart using our custom values of the version you want
$ helm install \
    ingress-nginx \
    --name nginx-ingress-controller \
    --values versions/v0.34.1/custom-values.yaml

# check
helm list
```


# Custom Values
The variables that can be used in the `custom-values.yaml` files are listed on [Github](https://github.com/kubernetes/ingress-nginx/tree/master/charts/ingress-nginx#configuration).


## Contributors
- Jorik Seldeslachts