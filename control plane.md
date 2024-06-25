The Kubernetes control plane in a Kubernetes cluster runs a collection of services that manage the orchestration functionality in Kubernetes.

From a learning perspective, it makes sense to use a single control plane in your test environment as you explore Kubernetes functionality. However, in production and cloud deployments such as Azure Kubernetes Service (AKS), you find that the preferred configuration is a high-availability deployment with three to five replicated control planes.

`Note`
`The fact that a control plane runs specific software to maintain the state of the cluster doesn't exclude it from running other compute workloads. However, you usually want to exclude the control plane from running noncritical and user app workloads.`

![Diagram of a Kubernetes cluster architecture that shows the components installed on the control plane.](https://learn.microsoft.com/en-us/training/modules/intro-to-kubernetes/media/3-cluster-architecture-master.svg)

The following services make up a Kubernetes cluster's control plane:
- [[API server]]
- Backing store
- Scheduler
- Controller manager
- Cloud controller manager