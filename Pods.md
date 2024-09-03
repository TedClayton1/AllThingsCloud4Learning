In cloud computing, a pod is ==a group of containers that share resources and work together as a single unit==. Pods are a fundamental unit for deploying and managing containerized applications in a Kubernetes environment. They are also known as clusters.

_Pods_ are the smallest deployable units of computing that you can create and manage in Kubernetes.

A _Pod_ (as in a pod of whales or pea pod) is a group of one or more [[Containers]] shared storage and network resources, and a specification for how to run the containers. A Pod's contents are always co-located and co-scheduled, and run in a shared context. A Pod models an application-specific "logical host": it contains one or more application containers which are relatively tightly coupled. In non-cloud contexts, applications executed on the same physical or virtual machine are analogous to cloud applications executed on the same logical host.

As well as application containers, a Pod can contain [[Init Containers]] that run during Pod startup. You can also inject [ephemeral containers](https://kubernetes.io/docs/concepts/workloads/pods/ephemeral-containers/) for debugging a running Pod.

 Pod is the atomic unit of deployment in Kubernetes. A Pod contains one or more containers and storage resources. Usually, there would be a single container within a Pod. Additional containers can be added to the Pod when we need small helper services. Each Pod has a unique IP address that is shared with the containers inside it. Pods are ephemeralby nature and are recreated when they need to be rescheduled. If they use no persistent volumes, the volume content vanishes when a Pod is recreated. To create a Pod, we use kind of Pod and define what image we want to use, like so:

apiVersion: v1
kind: Pod
metadata:
	name: my-pod
	labels:
	 app: myapp
	spec:
	 containers:
	 - name: my-container
	 image: nginx: 1.7.9

Here, we can see a definition of a Pod with a container that's been deployed from an nginx image.

