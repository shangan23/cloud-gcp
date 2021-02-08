# AppEngine

AppEngine comes with two type,
1. Standard
2. Flexible

## AppEngine Standard Environment

- Standard is simpler and fine grained autosclaing. Provide Free daily quota. AppEngine supports SDKs for testing locally and deploying to AppEngine. Runtime will be provided by Google and supports specific versions of Java, PHP, Python and Go. Enforces restriction code using `sandbox`. Sandbox is used for scaling. Sandbox cannot write to local disk, 60 sec timeout for installation, third party lib is not supported. Application can use several service provided by GCP.

## AppEngine Flexible Environment

- AppEngine flexible allows to specifies docker container instead of running in sandbox with Standard. AppEngines mangages compute engines updates,security, health checked and can let you choose geo location to run. Works for any programming language. Datastore, memcache, task queue and so on.

## Compare Environments and Engine

- Standard Vs Flexible Env

!(Standard Vs Flexible)[../images/AppEngineEnvironmentComparison.png]

- App Engine Vs Kubernetes Engine

!(App Vs Kubernetes)[../images/AppEngineEnvironmentComparison.png]

## Apigee Edge
You want to gradually decompose a pre-existing monolithic application, not implemented in GCP, into microservices. You want to do business analytics and billing on a customer-facing API. 

## Cloud Endpoints
You want to support developers who are building services in GCP through API logging and monitoring.