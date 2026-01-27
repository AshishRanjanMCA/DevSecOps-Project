# Master Node Setup

## Responsibilities
The Kubernetes Master Node (Control Plane) is responsible for:
- Initializing and managing the Kubernetes cluster
- Controlling cluster state and scheduling decisions
- Exposing the Kubernetes API server
- Managing worker node registration

---

## Key Setup Steps

### 1. Install Container Runtime
Install the required container runtime dependencies to enable Kubernetes to run containers.

---

### 2. Install Kubernetes Components
Install the following Kubernetes tools on the master node:
- **kubeadm** – Used to initialize and manage the cluster
- **kubelet** – Node agent that manages Pods
- **kubectl** – Command-line tool to control the cluster

---

### 3. Initialize the Cluster
Initialize the Kubernetes cluster using `kubeadm`:

```bash
kubeadm init
This command:

Sets up the control plane

Generates cluster certificates

Starts core Kubernetes components

4. Generate Worker Node Join Command
After initialization, kubeadm generates a join command that is used by worker nodes to connect to the cluster:

kubeadm join <master-ip>:6443 --token <token> --discovery-token-ca-cert-hash sha256:<hash>

## Outcome
- Kubernetes control plane is successfully initialized
- API server is accessible
- Worker nodes can join the cluster using the generated command
