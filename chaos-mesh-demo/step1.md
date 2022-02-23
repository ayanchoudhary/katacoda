Minikube has been installed and configured in the environment. Check that it is properly installed, by running the minikube version command:

`minikube version`{{execute}}

Start the cluster(with 2 nodes), by running the minikube start command:

`minikube start --nodes 2`{{execute}}

Great! You now have a running Kubernetes cluster in your online terminal. Minikube started a virtual machine for you, and a Kubernetes cluster is now running in that VM.

Details of the cluster and its health status can be discovered via: 

`kubectl cluster-info`{{execute}}

To view the nodes in the cluster using:

`kubectl get nodes`{{execute}}