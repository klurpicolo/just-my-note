# Kubernetes 
Kubernetes or K8s is container orchestration tool. It provides many useful solution of scaling , service discovery, configuration and secret management and so on.

## Why we need Kuberetes
For simple application, we can just docker run or docker-compose to deploy. But for load intensive, high availablity application, Kubernetes gives us tools to achieve that.

## Terminology
- Worksloads
  - Node : Machine(vistual or physical) that used for run Pods
  - Pod : Pod is a group of one or more containers. It can be considered as wrapper of Container(s). Normally, we don't deploy Pod directly but rather create Pod using workload resources such as Deployment, Job or StatefulSet
- Network
  - Service : This give abstract way to expose application without knowing the Pod being behind.
  - Ingress : Ingress is specification of proxy used for expose Service. It can be used for routing, load balancer, WAF and so on.
  - IngressController : This is actual implementation of Ingress, without this Ingress can't be used. 
One of famous IngressController is Nginx.
- Workload resources
  - Deployment : It's instruction of desired state of application. We can set how many pod to deploy, deployment strategy and so on.
  - StatefulSet : Similar to Deployment but for stateful applications such as database. 
  - DaemonSet : DaemonSet ensures that Nodes(or somes) run a copy of Pad. One of use cases is log collector.
- Configuration
  - ConfigMap : ConfigMap is key-value pairs data that can be injected to Pod. Pods can consumes ConfigMaps as env variables, cmd arguments or configuration files.
  - Secret : Similar to ConfigMap but for sensitive data. Eg. TLS secrets, database password
- Kubernetes Objects : 
  K8s can describe in YAML file with 4 required fields.
  - apiVersion : version of K8s api.
  - kind : type of K8s object. Eg. Pod, Serivce.
  - metadata : data helps to identify object 
    - labels : key-value pairs that used for describe object. Eg. name, version, managed-by. Labels can be used for select objects(think of tags).
    - annotations : key-value paris used for add some metadata for others(human or K8s object) to get metadata.
  - spec : the desired state of object. details depends on type of K8s object.
    - selector : we can select K8s object using labels.