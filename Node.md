A node in a [[Kubernetes]] cluster is where your compute workloads run. Each node communicates with the [[control plane]] via the [[API server]] to inform it about state changes on the node.

There are several services that run on a Kubernetes node to control how workloads run.

![Diagram of a Kubernetes cluster architecture that shows the components installed on a Kubernetes node.](https://learn.microsoft.com/en-us/training/modules/intro-to-kubernetes/media/3-cluster-architecture-node.svg)

The following services run on the Kubernetes node:

- Kubelet
- Kube-proxy
- Container runtime