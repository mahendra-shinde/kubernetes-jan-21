# Kuberenetes Code of conducts

1. A Pod in ONE group/app cannot / should not communicate with POD in another application.
2. A communicate between TWO un-related pods MUST always happen VIA "service".
3. Pods frequentlty DIE!!! 
4. When a new POD replaces an OLD POD, it's IP address changes!!


## Service types:

* ClusterIP

    1. ClusterIP is default service type. Used only for internal communication.
    2. Has unique VIP (Virtual IP) and DNS name `servicename.namespace`

* NodePort

    1. An Extension to ClusterIp service
    2. Other than default properties of ClusterIP, NodePort has a special port with name "nodePort"
    3. Common service type in "On-premise" kubernetes.
    4. An additional "Reverse Proxy" setup is required. HAProxy, NGINX, Apache-HTTPD

* LoadBalancer

    1. An extension to NodePort service.
    2. It uses the native "Load-balancer" in cloud to setup load-balancer.  
