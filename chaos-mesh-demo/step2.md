Next step involves installing [Helm](https://helm.sh/docs/intro/install/). You can install Helm by running the following command:

`curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
chmod 700 get_helm.sh
./get_helm.sh
`{{execute}}

To check whether Helm is installed or not, execute the following command:

`helm version`{{execute}}

Now that we have Helm installed we can use it to install Chaos-Mesh in our cluster.