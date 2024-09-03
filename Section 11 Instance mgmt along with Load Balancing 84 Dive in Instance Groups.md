Advantages of [[MIG]]:

***High Availability for Production** - VM in the group stops, crashes, or is deleted by an action other than an instance group management command, the MIG automatically recreates that VM in accordance with the original instance specs.*

***Auto-healing via Health-Check** - User can also set up autohealing policy that relies on an application-based health check, which periodically verifies that your app responds as expected on each of the MIG's instances. If an app is not responding on a VM, that VM is automatically recreated.*

***Regional Coverage** - Regional MIGs let user spread app across multiple zones. This replication protects against zonal failures.*

***Load balancing** - MIGs work with load balancing services to distribute traffic across the instance group. 

***Scalability** - If Application require additional compute resources, autoscaled MIGs can automatically grow the number of instances in the group to meet demand.*
*If demand drops, autoscaled MIGs can automatically shrink to reduce your costs.*

***Automated Updates** - MIG automatic updated lets you safely deploy new versions of software to instances.* 

***Support for stateful workloads**- You can use MIGs for building highly available deployments and automating operation of applications with stateful data or configuration, i.e databases, DNS servers, long-running batch computations with checkpointing. Stateful MIGs preserve each instances unique state on machine restart, recreation, auto-healing, or update.*


Unmanaged Instance Groups:


