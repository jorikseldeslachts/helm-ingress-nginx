# helm-ingress-nginx

## About
Customized version of ingress-nginx Kubernetes ingress controller.
This project will provide helm charts for current and future versions of the ingress controller.
It is meant to be used by my Kubernetes-Ansible project.


## Official repository vs helm/stable
The `kubernetes/ingress-nginx` project is maintained by the `Kubernetes` project on [Github](https://github.com/kubernetes/ingress-nginx/) and has its own [helm charts](https://github.com/kubernetes/ingress-nginx/tree/master/charts/ingress-nginx) available. Even though this works perfectly it is recommended to use the charts provided by the official [stable helm repository](https://github.com/helm/charts/tree/master/stable/nginx-ingress). These can be fine tuned a little more and have some more options available.


## Install Helm 3
Install `Helm 3` on your machine using the instructions on [helm.sh](https://helm.sh/docs/intro/install/).
```sh
# download and install helm binary
$ curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
$ chmod 700 get_helm.sh
$ ./get_helm.sh
```


## Custom Values
The variables that can be used in the `custom-values.yaml` files are listed on [Github](https://github.com/helm/charts/tree/master/stable/nginx-ingress#configuration).


## Install helm chart
```sh
# Install the helm chart using our custom values of the version you want
$ helm install igc stable/nginx-ingress \
    --values versions/v0.34.1/custom-values.yaml

# Check
$ helm list
```


## Contributors
- Jorik Seldeslachts