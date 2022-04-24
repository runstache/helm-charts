# Postgres Database Chart

Helm Chart to deploy a Postgres Database Server to a local Kubernetes cluster.

## Resources

The chart will deploy the followings resources:

* Kubernetes Deployment
* Kubernetes Service

## Values

The values available for Helm deployment are as follows:

* __replicas__: Denotes the number of Replica Pods to deploy. (default: 1)
* __image.repository__: Image Repository name. (default: postgres)
* __image.tag__: Docker Image Tag. (default: latest)
* __image.pullPolicy__: Denotes when to pull a new image copy. (default: IfNotPresent)
* __service.type__: Denotes the type of Kubernetes service to deploy. (default: LoadBalancer)
* __database.name__: Sets the default name of the database to create on the Postgres server. (default: postgres)
* __database.user__: Sets the Root Username. (default: admin)
* __database.password__: Sets the Root password. (default: password)
* __database.port__: Denotes the port to expose for connecting to the server. (default: 5432)
* __resources.requests.cpu__: Specifies the initial resource request for CPU resources (default: 100m)
* __resources.requests.memory__: Specifies the initial resource request for Memory resources (default: 512Mi)
* __resources.limits.cpu__: Specifies the limit for CPU usage. (default: 500m)
* __resources.limits.memory__: Specifies the limit for Memory usage. (default: 1Gi)
