## Kubectl
Use for interact with cluster, from read pods specification to create new resources.
example
kubectl get [resourceType|CRD]
kubectl describe [resourceName|CRD]

### Tricks
- kubectl run curl-test --image=radial/busyboxplus:curl -i --tty --rm
  run a single pod of busyboxplus for curl or investigation inside cluster

## Kubens
Use for list and select the current working namespace. It helps to avoid tedious task to put namespace for every K8s cli.

## Kubectx
๊๊๊Use for set K8s context, change cluster that currently working with.