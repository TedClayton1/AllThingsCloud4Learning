A container is a standard unit of software that packages up code and all it's [[dependencies]] so the application runs quickly and reliably from 1 computing environment to another. Container is the process which is executing your application code with it all dependencies. Containers **virtualize multiple application runtime environments on the same operating system instance, providing isolation and portability**.


To understand containers, let's compare them with virtual machines. While virtual machines virtualize hardware, containers virtualize the operating system. They abstract the application, along with all its dependencies, into one unit. 

Multiple containers can be hosted on one operating system running as an isolated process: Containers bring the following advantages: Isolation: Applications can use their own libraries without conflicting with libraries from other applications. Resource limitation: Applications can be limited to the resource's usage. Portability: Applications are self-contained with all dependencies and are not tied to an OS or a cloud provider. Lightweight: The footprint of the application is much smaller as the containers share a kernel.

![[Pasted image 20240709152116.png]]

Containers bring the following advantages:

**Isolation*: Applications can use their own libraries without conflicting with libraries from other applications. 

**Resource limitation**: Applications can be limited to the resource's usage.

**Portability**: Applications are self-contained with all dependencies and are not tied to an OS or a cloud provider.

**Lightweight**: The footprint of the application is much smaller as the containers share a kernel.