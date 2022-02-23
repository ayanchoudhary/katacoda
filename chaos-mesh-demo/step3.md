Before we start the installation we will create a custom namespace `chaos-mesh` to install chaos-mesh workloads into it via the command:

`kubectl create ns chaos-mesh`{{execute}}

Now that we have helm installed and have our custom namespace created we will use it to install chaos mesh in our Kubernetes cluster:

`helm repo add chaos-mesh https://charts.chaos-mesh.org
helm search repo chaos-mesh
helm install chaos-mesh chaos-mesh/chaos-mesh -n=chaos-mesh --version 2.1.3
`{{execute}}

We have used docker as the driver in this case, but you can use other drivers as well. Refer to the [Chaos-Mesh installation guide](https://chaos-mesh.org/docs/production-installation-using-helm/) for more details.

To check the running status of Chaos Mesh, execute the following command:

`kubectl get po -n chaos-mesh`{{execute}}