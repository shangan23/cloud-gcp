# Containers

## Container 
   - It is alternative to hardware VMs. Containers uses modern OS built in capabilities to isolate env from one anohter. A process is running program. In OS memory program is isolated take advantages of having it's own namespaces and supervisor. Deploying a containerized application consumes less resources and is less error-prone than deploying an application in virtual machines.Kubernetes engine uses the docker container runtime. A container provides
    - Package app into minimal size component
    - Abstract away unimportant details
    - Containers are loosely coupled to their environments
    - easy to deploy 

## Kubernetes 
  - Containers are very efficient abstraction. Google uses Kubernetes for managing the containers. Kubernets use concepts called `pod`. Group of containers can be deployed in a `pod`. Rolling updates without downtime. 

 ## Kubernetes Cluster 
  - A group of machines where Kubernets can schedule containers. Those machines are called `nodes`. Clusters can node spread across zone's for resilent behaviour. Built in load balancing and scale up capabilities get routed to the ingress port.  A Kubernetes cluster is a group of machines where Kubernetes can schedule containers in pods. The machines in the cluster are called “nodes.”

 ## Kubernetes Engine 
  - Lets you build, manage, resize and delete Kubernetes cluster. Cluster nodes and master run on Compute engine. It's a managed service. Has built in logging and monitoring capabilites. Auto updates master selection in Kubernets cluster. Google provides Containter Build and Container Registry. The Kubernetes Engine team periodically performs automatic upgrades of your cluster master to newer stable versions of Kubernetes, and you can enable automatic node upgrades too. Because the resources used to build Kubernetes Engine clusters come from Compute Engine, Kubernetes Engine gets to take advantage of Compute Engine’s and Google VPC’s capabilities.
