
The master node takes care of maintaining the desired state of the cluster. It monitors the Kubernetes object definitions (YAML files) and makes sure that they are scheduled on the worker nodes. YAML Ain't Markup Language (YAML) is a human-friendly data serialization standard, mainly used for configuration files. It is an alternative for formats such as XML or JSON.

It is essentially a control plane for the cluster. It works as follows:


![[Pasted image 20240709160744.png]]

The master node runs multiple processes:

**API server**: Exposes the Kubernetes API. It is the frontend of the control plane. 

**Controller manager**: Multiple controllers are responsible for the overall health of the cluster.

**etcd**: A database that hosts the cluster state information.

**Scheduler**: Responsible for placing the Pods across the nodes to balance resource consumption.

A cluster can run perfectly with just one master, but multiple nodes should be run for high availability and redundancy purposes. Without the master, the control plane is essentially down. All the cluster management operations you perform go through the master API. So, for production workloads, it is recommended that you have multiple master configurations. 

**Worker nodes**

A worker node can be a virtual machine or even a physical server. In the case of GKE, it is a virtual machine instance. Worker nodes are responsible for running containerized applications. Worker nodes are managed by the master node. They run the following services:

**Kubelet**: This reads the Pod specification and makes sure the right containers run in the Pods. It interacts directly with the master node.

**Kube-proxy**: This is a network proxy running on each node. It enables the usage of services (we will learn about services shortly).

**Container runtime**: This is responsible for running containers. Kubernetes supports multiple runtimes but in the case of GKE, Docker is used.