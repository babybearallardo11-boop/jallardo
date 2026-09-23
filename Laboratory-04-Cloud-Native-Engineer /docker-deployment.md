
# Docker Deployment and Container Lifecycle

## Executed Deployment Commands

```bash
# 1. Download the official Nginx image from Docker Hub
docker pull nginx

# 2. Run the Nginx container in detached mode mapping host port 8080 to container port 80
docker run -d -p 8080:80 --name my-web-server nginx

# 3. Verify the server is running by making an HTTP request locally
curl http://localhost:8080
