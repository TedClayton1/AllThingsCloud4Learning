In Google Cloud Platform (GCP), an instance group is a collection of virtual machine (VM) instances that can be managed as a single entity. Compute Engine offers two types of instance groups: managed instance groups (MIGs) and unmanaged instance groups:

- Managed instance groups (MIGs)
    
    These groups allow you to run applications on multiple identical VMs. MIGs can help with reliability, scaling, health, and change management. They can also help applications handle increased traffic and reduce costs when resources are not needed as much. MIGs can include automated services like auto-scaling, auto-healing, regional deployment, and automatic updating. For example, regional MIGs can spread app load across multiple zones to protect against zonal failures. MIGs can also be used to automate the operation of applications with [[stateful data]] or configuration, such as databases, DNS servers, and long-running batch computations.
    
- Unmanaged instance groups
    
    These groups are for instances that you want to group together but manage individually. Unlike MIGs, unmanaged instance groups are collections of distinct VMs that do not share a common instance template.
- Groups of dissimilar Instances that user can add remove from the Group.
- Do not offer Auto Scaling, AutoHealing or rolling Update kind of features.
- Not recommended, used only when user need to apply load-balancing to pre-exists configuration

*All the machines, which are part of a single instance group. They must be connected with a [[load balancer]].

*Any change in the instance group changes all instance of IG.

*Instance group is used to avoid individual instance management in a project.

