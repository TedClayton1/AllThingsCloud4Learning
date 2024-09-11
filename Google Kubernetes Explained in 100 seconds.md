Kubernetes is a tool for managing and automating containerized workloads in the cloud.
Imagine you have an orchestra, think of each individual musician as a container(a unit of software
that packages an application and everything it needs to run, such as libraries, dependencies and app code) (docker)
to create beautiful music we need a conductor to manage the musicians and set the tempo(Kubernetes).
Now imagine the conductor as kubernetes and the orchestra as an app like robinhood when the markets are
closed an app like robinhood isn't doing shit. But, when it opens it needs to fullfill millions
of trades for overpriced stock like tesla etc.

Kubernetes is the tool that orchestrates the infrasturcture to handle the changing workload.It can scale
containers across multiple machines "auto scale" and if one fails it knows how to replace it with a new one 
"auto heal" . A system deployed on kubernetes is knows as a cluster (a group of computing nodes/worker machines
that run a containerized application). The brain of the operation is known
as a "control plane" as it exposes an API server that can handle both internal/external requests to manage
the cluster. It also contains its own key value database "ETCD" which stores data about running the cluster.

What it's managing is one or more worker machines called "nodes". WHen you hear nodes think of a machine. Each
node is running something called a kublet which is a tiny app that runs on the machine to communicate back with 
the main control plane mothership. Inside of each node we have multiple pods which is the smallest deployable unit
in kubernetes. When you hear pod think of a pod of whales or containers running together. As the workload increases
kubernetes automatically scales horizontally by adding more nodes to the cluster it takes care of complicated
things like : networking, secret management, persistent storaage.

It is designed for high availability. 1 way it achieves that is with a replica set. Which is a set of running
containers ready to go at any given time. AS a developer you define objects in yaml that describe the desired state
of your cluster. For example we might have a nginx deployment that has a replica set with 3 pods. In the spec field we can state
how it should behave like its containers, volumes and ports and so on.

You can then take this configuration and use it to provision and scale containers automatically and ensure they're always up and 
running/healthy.
