Kubernetes is an open-source platform designed to automate the deployment, scaling, and management of containerized applications. It originated from Google's experience with container orchestration and has become a widely adopted system for managing applications running in containers across clusters of machines[1][2].

## Core Concepts of Kubernetes

**1. Containers and Pods**  
- Containers are lightweight, isolated environments that package an application and its dependencies.  
- Kubernetes does not run containers directly on nodes but wraps them inside *Pods*, which are the smallest deployable units in Kubernetes. A Pod can host one or multiple containers that share the same network and storage resources and run on the same node[3][5].

**2. Nodes and Cluster**  
- A *Kubernetes cluster* is a group of machines called *nodes* that run containerized applications. Nodes can be physical or virtual machines and are categorized as:  
  - *Master (Control Plane) nodes*: Manage the cluster and make global decisions.  
  - *Worker nodes*: Run the actual application Pods[3][4][6].

**3. Control Plane Components**  
- The control plane manages the cluster's overall state and consists of:  
  - **kube-apiserver**: The front-end API server that exposes the Kubernetes API.  
  - **etcd**: A distributed key-value store that holds all cluster data and configuration.  
  - **kube-scheduler**: Assigns Pods to nodes based on resource availability and constraints.  
  - **kube-controller-manager**: Runs controllers that ensure the desired state of the cluster matches the actual state (e.g., managing replicas of Pods)[3][4][6].

**4. Worker Node Components**  
- Each worker node runs:  
  - **kubelet**: An agent that communicates with the control plane and ensures containers in Pods are running as expected.  
  - **Container runtime**: Software like Docker or containerd that runs containers.  
  - **kube-proxy**: Handles network communication inside and outside the cluster[3][5].

## Key Features and Benefits

- **Declarative Configuration and Desired State Management**: Users define the desired state of applications (e.g., number of replicas, container images) using YAML or JSON files. Kubernetes continuously works to maintain this state, automatically creating, updating, or deleting Pods as needed[2][6].

- **Service Discovery and Load Balancing**: Kubernetes can expose containers via DNS names or IP addresses and balance network traffic to maintain stability under load[2].

- **Automated Rollouts and Rollbacks**: Kubernetes manages updates to applications smoothly, allowing for controlled rollouts and the ability to revert to previous versions if necessary[2][6].

- **Self-Healing**: Kubernetes automatically restarts failed containers, replaces unresponsive ones, and ensures only healthy Pods receive traffic[2].

- **Horizontal Scaling**: Applications can be scaled up or down manually or automatically based on CPU usage or other metrics[2][6].

- **Storage Orchestration**: Kubernetes can automatically mount storage systems, including local storage or cloud providers[2].

- **Secret and Configuration Management**: Sensitive information like passwords and tokens can be securely stored and managed without rebuilding container images[2].

## How Kubernetes Works in Practice

- You create a cluster of nodes.  
- Deploy your containerized application inside Pods on worker nodes.  
- Use Kubernetes API or command-line tool (`kubectl`) to manage your apps.  
- Kubernetes schedules Pods on nodes, monitors their health, and manages networking and storage.  
- If a Pod crashes or a node fails, Kubernetes reschedules Pods to maintain the desired state[1][3][6].

In summary, Kubernetes provides a robust framework for running containerized applications reliably and at scale, automating many operational tasks and enabling continuous deployment and scaling in modern cloud-native environments[1][2].

Citations:
[1] https://kubernetes.io/docs/tutorials/kubernetes-basics/
[2] https://kubernetes.io/docs/concepts/overview/
[3] https://www.okteto.com/blog/kubernetes-basics/
[4] https://www.youtube.com/watch?v=r2zuL9MW6wc
[5] https://www.youtube.com/watch?v=TlHvYWVUZyc
[6] https://www.redhat.com/en/topics/containers/learning-kubernetes-tutorial

---
Respuesta de Perplexity: pplx.ai/share