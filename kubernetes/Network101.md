# Network
For bare Docker application, We have to expose port to host machine then another application can access it using hostIP:port. This is find but not suit well in cluster environment like K8s. 

## Service
Service is an abstraction layer on top of Pod. It helps application client to access application(Pod) without knowing Its location(IP). For external access, see Ingress.


|Feature/Type|ClusterIP|NodePort|LoadBalancer|
|------------|---------|--------|------------|
| Access from | Only in cluster | Access using any cluster node IP | Access using LB IP |
| How to access | serivce-name:port | clusterIP:nodePort | LoadBalanceIP:Port
