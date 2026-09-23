
# 🚀 Mission 4: The Cloud-Native Engineer

> **Module:** CCM101 – Cloud Computing Laboratory  
> **Repository Directory:** `Laboratory-04-Cloud-Native-Engineer`  
> **Author:** Jhon Carlo C. Allardo  

---

## 📋 Mission Overview
At CloudNova Technologies, modern cloud operations demand moving beyond heavyweight Virtual Machines (VMs). As part of the Cloud-Native Engineering Team, this lab focuses on containerization—exploring how Docker enables lightweight, portable, and rapid application deployment compared to traditional hypervisor-based virtualization.

Using the **KillerCoda** interactive Linux playground, this activity walks through the hands-on process of fetching container images, configuring network port forwarding, monitoring active runtime containers, and cleanly managing container lifecycles.

---

## 🎯 Key Objectives
- **Architecture Analysis:** Differentiate between hardware-level hypervisors (VMs) and OS-level virtualization (Containers).
- **Environment Setup:** Provision and verify an isolated Docker environment on an Ubuntu cloud node.
- **Service Deployment:** Fetch and spin up an Nginx web server using Docker CLI commands.
- **Port Binding:** Forward host traffic to internal container ports (`-p 8080:80`).
- **Lifecycle Control:** Practice starting, auditing, halting, and purging containers.
- **Technical Documentation:** Maintain a structured, evidence-backed GitHub Cloud Computing portfolio.

---

## 🛠️ Docker Operations Log

| Command | Action Type | Purpose / Description |
| :--- | :--- | :--- |
| `docker --version` | Audit | Verifies the installed Docker Client version on the host. |
| `docker info` | Audit | Displays system-level engine configuration, storage drivers, and active containers. |
| `docker pull nginx` | Fetch | Retrieves the official Nginx base image from Docker Hub. |
| `docker run -d -p 8080:80 --name my-web-server nginx` | Execution | Launches Nginx in detached mode, exposing host port 8080 to container port 80. |
| `curl http://localhost:8080` | Verification | Issues a local HTTP GET request to verify Nginx serves its default welcome page. |
| `docker ps` | Monitoring | Filters and lists all currently running containers. |
| `docker stop my-web-server` | Control | Sends `SIGTERM` to gracefully shutdown the running Nginx container. |
| `docker ps -a` | Monitoring | Displays all container records on the host (both running and terminated). |
| `docker rm my-web-server` | Cleanup | Permanently deletes the stopped container instance to free up resources. |

---

## 📸 Technical Evidence & Screenshots

### Checkpoint A: Environment Verification
> Confirmed Docker daemon operational status inside KillerCoda.
![Docker Version](screenshots/docker-version.png)

### Checkpoint B: Nginx Container Deployment
> Successfully deployed container and fetched HTTP response via local `curl`.
![Nginx Running](screenshots/nginx-running.png)

### Checkpoint C: Lifecycle Management
> Executed container lifecycle state transitions (list, stop, audit, remove).
![Container Lifecycle](screenshots/container-lifecycle.png)

---

## 💡 Engineering Takeaways

- **Kernel Sharing vs. Emulation:** Containers leverage the host system's Linux kernel, drastically reducing boot overhead from minutes to seconds.
- **Isolated Networking:** Containers are isolated by default; explicit port mapping (`-p`) is critical to bridging external traffic into isolated container namespaces.
- **Stateless/Ephemeral Architecture:** Container file systems are temporary. Stopping or removing a container deletes un-volumed data, driving home the cloud-native pattern of keeping applications stateless.

---

## ⚡ Challenges & Troubleshooting

1. **Port Exposure Understanding:** Configured `-p 8080:80` to bridge local host traffic to Nginx's internal HTTP daemon port.
2. **Resource Hygiene:** Observed that stopping a container (`docker stop`) keeps its configuration state on disk until explicitly purged with `docker rm`.
