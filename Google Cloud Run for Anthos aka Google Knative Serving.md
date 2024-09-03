
Google Knative serving is ==a managed service that simplifies the process of building and deploying serverless workloads across multi-cloud and hybrid environments==. It abstracts away the complexity of Kubernetes and focuses on features like deployment, scaling, and network topology. 

Knative serving defines a set of objects called Kubernetes Custom Resource Definitions (CRDs) that control how serverless workloads behave on the cluster. The main resource is the service, which is a single application that manages the entire lifecycle of a workload. Each service is located in a specific GKE cluster namespace and exposes a unique endpoint. Services automatically scale the underlying infrastructure to handle incoming requests. 

Here are some of the features of Knative serving: 

- Revisions
    
    Immutable snapshots of code and configuration taken at a specific point in time. Each time a service is updated, a new revision is created. 
    
- Configurations
    
    Maintain the current settings for the latest revision and record a history of all previous revisions. Modifying a configuration creates a new revision. 
    
- Routes
    
    Define an HTTP endpoint and associate it with one or more revisions to which requests are forwarded. 
    
- Networking layers
    
    Support multiple networking layers, such as Ambassador, Contour, Kourier, Gloo, and Istio, for integration into existing environments. 
    
- Rollouts
    
    Enable developers to reveal new container upgrades to a portion of the user base and gradually increase the audience as issues are resolved.