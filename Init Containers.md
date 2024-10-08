

This page provides an overview of init containers: specialized containers that run before app containers in a [[Pods]]. Init containers can contain utilities or setup scripts not present in an app image.

## Understanding init containers[](https://kubernetes.io/docs/concepts/workloads/pods/init-containers/#understanding-init-containers)

A [Pod](https://kubernetes.io/docs/concepts/workloads/pods/) can have multiple containers running apps within it, but it can also have one or more init containers, which are run before the app containers are started.

Init containers are exactly like regular containers, except:

- Init containers always run to completion.
- Each init container must complete successfully before the next one starts.

If a Pod's init container fails, the kubelet repeatedly restarts that init container until it succeeds. However, if the Pod has a `restartPolicy` of Never, and an init container fails during startup of that Pod, Kubernetes treats the overall Pod as failed.

To specify an init container for a Pod, add the `initContainers` field into the [Pod specification](https://kubernetes.io/docs/reference/kubernetes-api/workload-resources/pod-v1/#PodSpec), as an array of `container` items (similar to the app `containers` field and its contents). See [Container](https://kubernetes.io/docs/reference/kubernetes-api/workload-resources/pod-v1/#Container) in the API reference for more details.

The status of the init containers is returned in `.status.initContainerStatuses` field as an array of the container statuses (similar to the `.status.containerStatuses` field)