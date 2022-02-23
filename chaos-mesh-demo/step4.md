Now that we have our Kubernetes cluster setup and we have chaos mesh installed we can now view their versions and execute a Chaos Experiment.

To check the specific versions execute the commands:

Kubernetes:
`kubectl version`{{execute}}

Chaos Mesh:
`helm search repo chaos-mesh`{{execute}}

Congrats! We can execute a Network-Delay Chaos-Experiment in our cluster using the configuration file.

```yaml
apiVersion: chaos-mesh.org/v1alpha1
kind: NetworkChaos
metadata:
  name: network-delay
spec:
  action: delay # the specific chaos action to inject
  mode: one # the mode to run chaos action; supported modes are one/all/fixed/fixed-percent/random-max-percent
  selector: # pods where to inject chaos actions
    namespaces:
      - default
    labelSelectors:
      'app': 'web-show' # the label of the pod for chaos injection
  delay:
    latency: '10ms'
  duration: '12s'
```

Execute the Chaos Experiment via the following command:
`kubectl apply -f network-delay.yaml -n chaos-mesh`{{execute}}

