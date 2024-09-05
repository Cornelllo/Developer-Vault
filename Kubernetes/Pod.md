A pod represents a single instance of an app running in Kubernetes. The workloads that you run on Kubernetes are containerized apps. Unlike in a Docker environment, you can't run containers directly on Kubernetes. You package the container into a Kubernetes object called a pod. A pod is the smallest object that you can create in Kubernetes.

![Diagram of a pod with a website as the primary container.](https://learn.microsoft.com/en-us/training/modules/intro-to-kubernetes/media/3-diagram-pod-with-website.svg)

A single pod can hold a group of one or more containers. However, a pod typically doesn't contain multiples of the same app.

A pod includes information about the shared storage and network configuration and a specification about how to run its packaged containers. You use pod templates to define the information about the pods that run in your cluster. Pod templates are YAML-coded files that you reuse and include in other objects to manage pod deployments.

![Diagram of pod with a website as the primary container and a supporting container. The node has both an assigned IP address and a localhost host address.](https://learn.microsoft.com/en-us/training/modules/intro-to-kubernetes/media/3-diagram-pod-with-website-database.svg)

For example, let's say that you want to deploy a website to a Kubernetes cluster. You create the pod definition file that specifies the app's container images and configuration. Next, you deploy the pod definition file to Kubernetes.

It's unlikely that a web app has a website as the only component in the solution. A web app typically has some kind of datastore and other supporting elements. Kubernetes pods can also contain more than one container.

Assume that your site uses a database. The website is packaged in the main container, and the database is packaged in the supporting container. Multiple containers communicate with each other through an environment. The containers include services for a host OS, network stack, kernel namespace, shared memory, and storage volume. The pod is the sandbox environment that provides all of these services to your app. The pod also allows the containers to share its assigned IP address.

Because you can potentially create many pods that are running on many nodes, it can be hard to identify them. You can recognize and group pods by using string labels that you specify when you define a pod.

### Lifecycle of a Kubernetes pod