# 🚀 Kubernetes Project 6: NGINX Pod with Resource Management

![Kubernetes](https://img.shields.io/badge/Kubernetes-v1.34-blue?logo=kubernetes)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📖 Project Overview

This project demonstrates how to deploy an application using a **Kubernetes Pod** with proper **CPU and Memory resource management** inside a custom namespace.

The goal is to understand how Kubernetes handles resource allocation using **requests** and **limits**.

---

## 🎯 Objectives

- Deploy a Pod using YAML configuration  
- Use a custom Docker image  
- Apply CPU & Memory resource constraints  
- Manage Pod lifecycle using `kubectl`  
- Work within a dedicated namespace  

---

## 🛠️ Tech Stack

- Kubernetes  
- Docker  
- kubectl CLI  
- YAML  

---

## 📂 Project Structure


skillfied-project-6/
│── nginx.yaml
│── README.md


---

## ⚙️ Configuration Highlights

- **Namespace:** `skillfied`  
- **Pod Name:** `myapp1`  
- **Container Image:** `933538/repo2026:nginx-v1.0`  
- **Port:** 80  

### 🔥 Resource Configuration

| Resource | Requests | Limits |
|----------|---------|--------|
| CPU      | 250m    | 500m   |
| Memory   | 128Mi   | 256Mi  |

---

## 🚀 Deployment Steps

### 1️⃣ Create Namespace

```bash
kubectl create namespace skillfied
2️⃣ Deploy Pod
kubectl apply -f nginx.yaml
3️⃣ Verify Pod Status
kubectl get pods -n skillfied
4️⃣ Detailed Pod Information
kubectl describe pod myapp1 -n skillfied
5️⃣ View Logs
kubectl logs myapp1 -n skillfied
6️⃣ Delete Pod
kubectl delete pod myapp1 -n skillfied
📌 Key Concepts
🔹 Pod

Smallest deployable unit in Kubernetes that runs containers.

🔹 Namespace

Used to isolate resources within a cluster.

🔹 Resource Requests vs Limits
Requests → Minimum resources required by container
Limits → Maximum resources container can use
⚠️ Common Mistakes (Avoid These)
Using cpus instead of cpu
Wrong spelling: requirments ❌ → requests ✅
Incorrect memory units (M ❌ → Mi ✅)
Not specifying namespace while checking pods
📸 Output

output screenshot here:

images/output.png
🧠 Learning Outcomes
Hands-on experience with Kubernetes Pods
Understanding resource allocation
Working with namespaces
Writing production-level YAML
👨‍💻 Author

Anurag Mishra

GitHub: https://github.com/Anurag842321
LinkedIn: https://linkedin.com/in/anuragmishra2831
