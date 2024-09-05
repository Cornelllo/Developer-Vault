Kubernetes is a portable, extensible open-source platform for your management and orchestration of containerized workloads. Kubernetes simplifies complex container-management tasks and provides you with declarative configuration to orchestrate containers in different computing environments. This orchestration platform gives you the same ease of use and flexibility you might already know from platform as a service (PaaS) or infrastructure as a service (IaaS) offerings.
[Source](https://learn.microsoft.com/en-us/training/modules/intro-to-kubernetes/2-what-is-kubernetes)
## Kubernetes architecture

An orchestrator is a system that deploys and manages apps.  A [[Cluster]] is a set of computers that work together and are viewed as a single system. You use Kubernetes as the orchestration and cluster software to deploy your apps and respond to changes in compute resource needs.

![Diagram of a Kubernetes cluster architecture that shows the components installed on the control plane and the worker nodes.](https://learn.microsoft.com/en-us/training/modules/intro-to-kubernetes/media/3-cluster-architecture-components.svg)

Key components of Kubernetes
- [[Cluster]]
- [[Node]]
- [[Pod]]

Container Runtime Interface (CRI) -