# Network
For bare Docker application, We have to expose port to host machine then another application can access it using hostIP:port. This is find but not suit well in cluster environment like K8s. 

## Type
- ClusterIP
- NodePort
- LoadBalancer