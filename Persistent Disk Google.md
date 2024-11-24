
Google Cloud Persistent Disk (GCP) is ==a block storage service that provides durable network storage for virtual machine (VM) instances==: 

- **Durability**
    
    Data is automatically stored redundantly across multiple physical disks to ensure data integrity and availability. 
    
- **Performance**
    
    Performance scales automatically with size, and you can resize or add more volumes to meet your needs. 
    
- **Flexibility**
    
    You can detach or move volumes to keep your data even after deleting VMs. You can also configure automatic backups or resize storage without disrupting your application. 
    
- **Disk types**
    
    You can choose from solid state drive (SSD) or hard disk drive (HDD) disks. 
    
- **Disk size**
    
    Single persistent disks can be up to 64 TB. 
    
- **Configuration options**
    
    You can choose from three types of persistent disks, including Standard, SSD, and Local SSD. 
    

GCP Persistent Disk is used with services like Google Compute Engine, Google Kubernetes Engine, and App Engine. It's a good choice for applications that depend on IaaS solutions