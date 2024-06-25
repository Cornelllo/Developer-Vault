You can think of the API server as the front end to your Kubernetes [[cluster]]'s [[control plane]]. All the communication between the components in Kubernetes is done through this API.

For example, as a user, you use a command-line app called `kubectl` that allows you to run commands against your Kubernetes cluster's API server. The component that provides this API is called `kube-apiserver`, and you can deploy several instances of this component to support scaling in your cluster.

This API exposes a RESTful API that you can use to post commands or YAML-based configuration files. YAML is a human-readable, data serialization standard for programming languages. You use YAML files to define the intended state of all the objects within a Kubernetes cluster.

For example, assume that you want to increase the number of instances of your app in the cluster. You define the new state with a YAML-based file and submit this file to the API server. The API server validates the configuration, save it to the cluster, and finally enact the configured increase in app deployments.