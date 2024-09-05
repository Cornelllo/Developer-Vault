A node in a [[Kubernetes]] cluster is where your compute workloads run. Each node communicates with the [[control lane AKA master node]] via the [[API server]] to inform it about state changes on the node.

There are several services that run on a Kubernetes node to control how workloads run.

![Diagram of a Kubernetes cluster architecture that shows the components installed on a Kubernetes node.](https://learn.microsoft.com/en-us/training/modules/intro-to-kubernetes/media/3-cluster-architecture-node.svg)

The following services run on the Kubernetes node:

- Kubelet - monitors the nodes and containers on them and listens instructions from the kube-apiserver.
- Kube-proxy - ensures the rules in place on the workers node to allow the containers running on them to reach or communicate with each other.
- Container runtime engine - is a software like Docker, ContainerD or RKT that can run containers in them.