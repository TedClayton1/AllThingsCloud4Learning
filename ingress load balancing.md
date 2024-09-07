Ingress load balancing is ==a way to control how external users access Kubernetes cluster services using a set of routing rules==. It's a simple and secure method for routing traffic, and it can provide a number of services, including: Load balancing, SSL termination, and Name-based virtual hosting.  

Here are some other things to know about ingress load balancing:  

- Ingress controller
    
    An ingress controller is responsible for fulfilling the ingress, usually with a load balancer.  
    
- Routing rules
    
    Ingress allows for flexible routing rule configuration, which can simplify the production environment.  
    
- Single point of entry
    
    Ingress provides a single entry point into a cluster or service, which can make it easier to manage applications and troubleshoot routing issues.  
    
- Cost
    
    Ingress can be less expensive than giving each service a cloud load balancer because it allows for mutualization of application hosting.  
    
- Cloud-managed Kubernetes clusters
    
    When using ingress on a cloud-managed Kubernetes cluster, its powers can be expanded.