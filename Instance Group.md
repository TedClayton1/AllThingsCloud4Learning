


An instance group in Google Cloud Platform (GCP) is ==a collection of virtual machine (VM) instances that can be managed as a single entity==. There are two types of instance groups in GCP: managed instance groups (MIGs) and unmanaged instance groups: 

- **Managed instance groups (MIGs)**
    
    These groups are made up of identical VMs that can be operated on together. MIGs can automatically scale, heal, and update, and can be deployed across multiple zones. 
    
- **Unmanaged instance groups**
    
    These groups allow you to load balance across a fleet of VMs that you manage yourself. VMs in unmanaged groups can have different configurations, images, or hardware. 
    

Instance groups can help applications handle traffic increases and reduce costs when resource needs are lower.