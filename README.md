# K8S‑Cluster

**Create your own Kubernetes cluster step by step**

---

## 🚀 Project Overview
This project is a simple and step-by-step guide to building a Kubernetes cluster. It's a great starting point for anyone learning DevOps, cloud-native tools, or container orchestration.

---

## 🔧 Tech Stack
- Kubernetes (k8s)
- Shell Scripts (setup, deployment)
- `kubectl`, `kubeadm`
- Docker / Container Runtime

---

## 📦 Installation & Setup  

### Prerequisites:
- Linux or macOS machine (for full cluster setup)
- `docker`, `kubeadm`, `kubectl`, and `kubelet` should be installed
- At least 2 GB RAM and 2 CPUs per node

### Step‑by‑Step Guide:
1. Clone this repository:
   ```bash
   git clone https://github.com/karimtamboli07/K8S-Cluster.git
   cd K8S-Cluster
   ```
2. Install required dependencies:
   ```bash
   sudo apt update
   sudo apt install docker.io kubelet kubeadm kubectl -y
   sudo systemctl enable --now docker kubelet
   ```
3. Initialize the master node:
   ```bash
   sudo kubeadm init --pod-network-cidr=10.244.0.0/16
   ```
4. Apply a network plugin (e.g., Flannel):
   ```bash
   kubectl apply -f <network-plugin‑yaml>
   ```
5. Join worker nodes (you will get the join command after init).

---

## 🌟 Features
- Complete walkthrough from cluster initialization to networking  
- Automation via shell scripts  
- Clear step-by-step documentation  
- Suitable for educational and learning purposes

---

## 🧪 Usage
Once your cluster is ready:
```bash
kubectl get nodes
kubectl get pods --all-namespaces
```
Ensure all pods are running and the node shows as READY.

---

## 🙋 Author
- **Karim Tamboli**  
  GitHub: [karimtamboli07](https://github.com/karimtamboli07)

---

## 🛠 Contributions
- Feel free to contribute via GitHub Issues or Pull Requests.
- Update the README, add new features, fix bugs—your contributions are welcome!

---

## 📌 Quick Reference Table

| Step | Description                        |
|------|------------------------------------|
| 1    | Clone the repo                     |
| 2    | Install Docker, kubeadm, kubectl   |
| 3    | Initialize master node             |
| 4    | Apply network plugin               |
| 5    | Join worker nodes                  |
| 6    | Verify cluster status              |
