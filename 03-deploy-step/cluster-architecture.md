# Kubernetes Cluster Architecture

The Kubernetes cluster follows a **master–worker architecture**, consisting of a **Control Plane** and multiple **Worker Nodes**.  
This design enables centralized management and distributed workload execution.

---

## Control Plane (Master Node)

The **Control Plane** is responsible for managing the overall state of the cluster and making scheduling decisions.

### Core Components
- **API Server**  
  Acts as the central entry point for all Kubernetes commands and cluster interactions.

- **Scheduler**  
  Assigns Pods to appropriate worker nodes based on resource availability and constraints.

- **Controller Manager**  
  Ensures that the desired state of the cluster matches the actual state by managing controllers such as node, replica, and endpoint controllers.

---

## Worker Nodes

Worker nodes are responsible for running application workloads in the form of Pods.

### Core Components
- **kubelet**  
  A node-level agent that communicates with the control plane and manages Pods on the worker node.

- **Container Runtime**  
  Runs and manages containers (e.g., Docker or containerd).

- **Pods**  
  The smallest deployable units in Kubernetes, consisting of one or more containers.

---

## Architecture Outcome
- Centralized cluster management through the control plane
- Scalable and resilient workload execution on worker nodes
- Automated scheduling, monitoring, and self-healing of applications
