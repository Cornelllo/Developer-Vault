The Kubernetes control plane in a Kubernetes cluster runs a collection of services that manage the orchestration functionality in Kubernetes it is a set of components responsible for managing the state and operations of the cluster. It is not part of the node pool, nor is it a single node; rather, it consists of multiple components that can run on one or more machines (often referred to as master nodes). These components collectively form the control plane, which orchestrates the entire Kubernetes cluster.

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

### Key Components of the Control Plane

1. **API Server (`kube-apiserver`)**:
    
    - The API server is the central management entity that provides the Kubernetes API. It is the front end of the Kubernetes control plane, handling all REST requests for managing Kubernetes objects, such as pods, services, and deployments.
2. **Controller Manager (`kube-controller-manager`)**:
    
    - The controller manager runs controllers that regulate the state of the cluster. Examples of controllers include the replication controller, node controller, and endpoints controller. These controllers ensure that the desired state of the cluster, as defined in the API server, matches the current state.
3. **Scheduler (`kube-scheduler`)**:
    
    - The scheduler is responsible for assigning newly created pods to nodes based on resource availability, affinity/anti-affinity rules, and other constraints. It ensures that the workload is balanced across the nodes in the cluster.
4. **etcd**:
    
    - `etcd` is a distributed key-value store that Kubernetes uses to store all its cluster data, including the configuration, state, and metadata of all the objects. It is a critical component for cluster state and consistency.
5. **Cloud Controller Manager (if applicable)**:
    
    - The cloud controller manager integrates Kubernetes with cloud-specific APIs and services, such as load balancers, storage, and networking. It allows Kubernetes to interact with the underlying cloud infrastructure.