# 🐳 Docker Deployment and Container Management

## 🖥️ Docker Environment

The Docker environment was accessed through the KillerCoda Playground. Before deploying Nginx, I first checked the Docker installation and confirmed that the Docker environment was available.

### 1. 🔍 Check Docker Version

docker --version

This command displays the version of Docker installed in the current environment.

### 2. 📊 Check Docker Environment Status

docker info

This command provides detailed information about the Docker environment, including the Docker server, containers, images, and other configuration details.

---

## 🚀 Nginx Deployment

### 3. 📥 Pull the Nginx Image

docker pull nginx

This command downloads the official Nginx image so it can be used to create a container.

### 4. ▶️ Run the Nginx Container

docker run -d --name nginx-server -p 8080:80 nginx

This command creates and starts an Nginx container in detached mode. It also maps port 8080 on the host to port 80 inside the container.

### 5. 🌐 Test the Nginx Web Server

curl http://localhost:8080

This command sends an HTTP request to the Nginx server and checks whether the web server is responding correctly.

---

## 🔄 Container Lifecycle

### 6. 📜 List Running Containers

docker ps

This command displays the Docker containers that are currently running.

### 7. ⏹️ Stop the Nginx Container

docker stop nginx-server

This command stops the running Nginx container without deleting it.

### 8. 🔍 Verify the Container Is Stopped

docker ps -a

This command displays all Docker containers, including stopped containers, allowing me to verify that nginx-server has stopped.

### 9. 🗑️ Remove the Nginx Container

docker rm nginx-server

This command removes the stopped Nginx container from the Docker environment.

### 10. ✅ Confirm the Container Was Removed

docker ps -a

This command lists all containers again to verify that the nginx-server container has been completely removed.

---

## ⚡ Docker Command Sequence

The commands used for the container lifecycle were:

docker ps
docker stop nginx-server
docker ps -a
docker rm nginx-server
docker ps -a

The sequence demonstrates the basic lifecycle of the Nginx container: checking the running container, stopping it, verifying its stopped status, removing it, and checking the container list again.

---

## 📝 Summary

This activity allowed me to practice the basic process of deploying and managing a Docker container. I started by checking the Docker environment, downloaded the Nginx image, and created an Nginx container with port mapping. After testing the web server, I used Docker commands to view, stop, verify, and remove the container. Using docker ps -a also helped me see the container even after it was stopped and confirm when it had been removed completely.
