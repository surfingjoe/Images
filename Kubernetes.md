![](https://github.com/surfingjoe/Images/blob/master/Kubernetes_Drawing.jpg)

# Kubernetes

Kubernetes is an open source orchestration tool developed by Google for managing microservices or containerized applications across a distributed cluster of nodes.  Kubernetes provides highly resilient infrastructure with zero downtime readying capabilities, automatic rollback, scaling and self-healing of containers (which consists of auto-placement, auto-restart, auto-replication, and scaling of containers on the basis of hardware usage.

**Kubernetes API Server**

The API server is the central touch point that is accessed by all users, automation, and components in the Kubernetes cluster. The API server implements a RESTful API over HTTP, performs all API operations, and is responsible for storing API objects into a persistent storage backend.  The Kubernetes API server validates and configures data for the API objects which include pods, services, replication controllers, and others. 

**ETCD CLUSTER**

A simple, distributed key value storage which is used to store the Kubernetes cluster data.  It is only accessible from the API server for security reasons.  Etcd is a crucial storage component for Kubernetes as it stores the entire state of the cluster: its configuration, specifications, and the statuses of the running workloads.

**Kubernetes Controller-manager**

The Kubernetes controller manager is a daemon that embeds the core control loops shipped with Kubernetes. In applications of robotics and automation, a control loop is a non-terminating loop that regulates the state of the system. In Kubernetes, a controller is a control loop that watches the shared state of the cluster through the API-server and makes changes attempting to move the current state towards the desired state. Examples of controllers that ship with Kubernetes today are the replication controller, endpoints controller, namespace controller, and service-accounts controller.

**Kubernetes scheduler**

The scheduler watches for newly created Pods that have no Node assigned. For every Pod that the scheduler discovers, the scheduler becomes responsible for finding the best Node to run the newly discovered POD.  The scheduler finds feasible Nodes for a Pod and then runs a set of functions to score the feasible Nodes and picks a Node with the highest score among the feasible ones to run the Pod. The scheduler then notifies the API server about this decision in a process called binding.

**Worker Node – kubelet**

The main service on a worker node, regularly taking in new or modified specifications and ensuring the pods and their containers are healthy and running in the desired state.  Within a Kubernetes cluster, the kubelet functions as a local agent that watches for pod specs via the Kubernetes API server.

**Worker Node – kube-proxy**

A proxy service that runs on each worker node to deal with individual host subnetting and expose services to networks outside of Kubernetes.  Kube-proxy maintains network rules on nodes.  These network rules allow network communication to your Pods from network sessions inside or outside of your cluster.

C**ontainer Runtime**

The container runtime is the software that is responsible for running containers.

