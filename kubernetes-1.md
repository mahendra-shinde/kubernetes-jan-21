# Kubernetes Master Components

1. API-SERVER   Communication between internal components, nodes & users (via kubectl)
2. KUBELET      Communicates with API-SERVER, And represents a NODE in cluster.
                When Kubelet stops sending information to API-Server, node is assumed to be DOWN.

# Kubernetes CLI


* `kubectl` is CLI Client for Kubernetes
* it can connect ANY kubernetes installations
* Requires a CONFIG file, expected location 
    Win & Mac `/Users/USERNAME/.kube/config`
    Linux   `/home/USERNAME/.kube/config`
* kubectl actually makes rest request on HTTPS to API-SERVER

## Command Syntax

```
$ kubectl [Verb/Action] [ObjectType] [ObjectName] 

# Example: Get All Nodes
$ kubectl get nodes -o yaml

# Example: Get Particular node information
$ kubectl describe node docker-desktop 
```
