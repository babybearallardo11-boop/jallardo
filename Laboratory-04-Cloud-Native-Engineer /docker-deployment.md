# 📦 Docker Deployment & Lifecycle Operations Log

**Target System:** Ubuntu 24.04.5 LTS (Kernel 6.8.0-139-generic)  
**Engine Version:** Docker v29.1.3  
**Container Deployed:** `nginx-server`  
**Engineer:** Jhon Carlo C. Allardo  

---

## 1. Web Server Deployment Sequence

To transition from traditional server setups to containerized microservices, the official Nginx web server was pulled and executed using the Docker Command Line Interface (CLI).

### Phase 1: Image Acquisition & Execution

```bash
# Step 1: Download the official Nginx image layers from Docker Hub
root@ubuntu:~$ docker pull nginx
Using default tag: latest
latest: Pulling from library/nginx
6b37362b3da7: Pull complete 
f1169c633cbc: Pull complete 
2056b40bae09: Pull complete 
f802f27d954b: Pull complete 
3326c3817340: Pull complete 
afa8dec48454: Pull complete 
46243d3234ed: Pull complete 
Digest: sha256:abe47724e466aeab9a345d8e46a221c2fa8953c7848bb4a3bd9976a7199f8cf2
Status: Downloaded newer image for nginx:latest
docker.io/library/nginx:latest

# Step 2: Run the container in detached mode with host port forwarding (8080 -> 80)
root@ubuntu:~$ docker run -d --name nginx-server -p 8080:80 nginx
d779e5e426a2a9bcae422fcecbb213493916e1b93336d3169454aebb6b47c559
