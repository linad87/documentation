# Live Assessment

The Runtime Live Assessment capability lets users view and search specific live runtime information based on various data fields, providing visibility into the entire runtime environment. With the Live Assessment filter, users can selectively identify specific risks or issues that require attention. To access the Live Assessment, simply navigate to the **Live Assessment** section under the **Runtime** menu.

The Live Assessments consists of the following:&#x20;

* **Runtime Objects**: Runtime objects are the components that are active and operating within your runtime environment. They encompass various elements such as images, workloads, and processes, which work together to support the execution of applications and services.
* **Workloads**: In Kubernetes, a workload consists of one or more containers running in Pods, representing the applications and services actively executing in your cluster. Workloads can be managed by various Kubernetes resources, such as Deployments, StatefulSets, DaemonSets, or Jobs, depending on the nature and requirements of the tasks
* **Processes**: Processes are individual executable instances running within a workload. Each process operates within the context of its associated image and workload, and they can be grouped based on their executables, execution locations, command arguments, images, and other attributes. The [Processes table](processes-table.md) in the Live Assessment feature provides detailed views and vulnerability information about these processes, allowing for precise monitoring and risk management.
* **Images**: [Images ](images.md)are packaged binary files that contain the necessary code, runtime, libraries, environment variables, and configuration files required to run applications. They are fundamental building blocks used to create containers in a runtime environment. Our Runtime Live Assessment allows users to trace these images back to their source in JFrog Artifactory, providing insights into their usage and associated vulnerabilities.

\








\


\
