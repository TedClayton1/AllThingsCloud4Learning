
Snapshots are global resources which means they are available to all the regions globally. This avoids the need to manually export and import snapshots between regions. A snapshot that was taken from a persistent disk attached to an instance in us-central will be instantly available in europe-west.

In cloud computing, a snapshot is ==a copy of a volume's contents at a specific point in time==. Snapshots are a quick and cost-effective way to protect data and restore it if it's lost. However, they are not a substitute for backups. 

Here are some things to know about snapshots:

- **How they work**
    
    Snapshots are logical views of data blocks within a volume. They don't replicate data or consume capacity until the data is modified. 
    
- **How to use them**
    
    Snapshots can be used to revert an instance to a previous state, or to revert a specific file to a previous version. 
    

- **How they differ from backups**
    
    Snapshots are more cost-efficient than backups, but reverting to a previous state deletes the latest version of data. 
    

- **How they differ from copies**
    
    Snapshots aren't copies of data, so to make copies of data, you can use backups or volume replication features. 
    

- **How to store them**
    
    Snapshots can be stored in a regional location or a multi-regional location. 
    

- **How they're used**
    
    Snapshots can be used for data management, such as to optimize real-time pricing.