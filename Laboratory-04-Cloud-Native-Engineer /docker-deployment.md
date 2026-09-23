# 📦 Docker Deployment & Lifecycle Management

## 1. Overview & Environment Setup
The containerization environment was established using the KillerCoda Playground platform. System readiness was verified by inspecting the underlying runtime properties, ensuring active communication with the Docker engine, and verifying host configuration details prior to application deployment.

---

## 2. Web Server Deployment & Testing

* **Image Acquisition:** The official Nginx base image was downloaded directly from Docker Hub to serve as the foundational blueprint for the application container.
* **Container Instantiation:** An instance named `nginx-server` was created and launched to run isolated in the background (detached mode). Port mapping was configured to link external traffic from host port `8080` directly to the internal web server port `80`.
* **Service Verification:** Network connectivity and HTTP response capability were tested by sending a web request to port `8080`. Successful delivery of the standard Nginx welcome page confirmed proper network translation and service functionality.

---

## 3. Container Lifecycle Management

The operational lifecycle of the container was managed through four primary stages:

1. **Active Monitoring:** The runtime list of active containers was checked to verify process health, assigned network ports, and runtime status.
2. **Graceful Halting:** A stop command was issued to cleanly terminate web server operations while preserving container data on disk.
3. **State Audit:** The system process list was audited across all states to confirm that the container was no longer actively running and had transitioned to a stopped status.
4. **Resource Cleanup:** The stopped container was permanently deleted from the environment, releasing system storage and clearing the instance footprint.

---

## 💡 Key Takeaways
This deployment successfully demonstrated the end-to-end container lifecycle: fetching an application blueprint, running an isolated web service, establishing port forwarding, testing service availability, halting process execution, and removing the instance to keep the host environment clean.
