A cluster is a set of computers that you configure to work together and view as a single system. The computers configured in the cluster handle the same kinds of tasks. For example, they'll all host websites, APIs, or run compute-intensive work.

A cluster uses centralized software that's responsible for scheduling and controlling these tasks. The computers in a cluster that run the tasks are called [[node]]s, and the computers that run the scheduling software are called [[control plane]]s.

![Diagram of a computer cluster that shows how a task is distributed via the control plane to three nodes and the interaction between the nodes.](https://learn.microsoft.com/en-us/training/modules/intro-to-kubernetes/media/3-diagram-cluster.svg)