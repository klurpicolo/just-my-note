# Helm
Helm is package manager for K8s application. It can be compare with YUM and APT in Linux or Homebrew for Mac. We can install K8s application by add repository and then install. If we want to package own application the deploy in K8s which might have complex K8s component setup. Helm can help us by organized it using template.

## Why we need Helm
When we deploy appliaction in K8s, usually we have to deploy Deployment, Service, ConfigMap and so on, depends on application design which is hard to do manually. Helm helps to simplify those step by provide template and ability to inject variable(value) to template.

## Terminology
- Chart : It is packaging format. Including a set of k8s definition depends on application and Chart definition file.

## Chart file structure (only important)
```
helm/
    Chart.yaml      # Contain metadata of Chart. Eg. Chart name, version
    values.yaml     # default configuration
    templates/      # K8s manifest
        deployment.yaml
        service.yaml
        ingress.yaml
        ...
```

## Install 
```
When install parameter in template will be replaced by value in values.yaml
templates/
    +   =>  Kubernetes manifest => Go into K8s
values.yaml
```