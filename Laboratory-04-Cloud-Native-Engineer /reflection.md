
# Mission Reflection

### 1. Boot Time and Setup Comparison
Installing an operating system on a Virtual Machine requires provisioning virtual hardware, booting an ISO installer, going through OS configuration steps, and initializing a full guest kernel, which typically takes anywhere from 5 to 15 minutes. In contrast, a Docker container shares the host system's Linux kernel and only packages application binaries and dependencies. As a result, launching a Docker container skips the entire OS boot sequence, enabling applications to start up in a fraction of a second.

### 2. Purpose of Port Mapping (`-p 8080:80`)
By default, Docker isolates container network environments from the host system. Port mapping using the `-p 8080:80` flag acts as a bridge or reverse proxy; it forwards external traffic arriving at port `8080` on the host machine directly to port `80` (the default HTTP web port) inside the isolated container. Without this explicit mapping, the Nginx web server running inside the container would remain unreachable to network traffic outside its private container network.

### 3. Impact of `docker rm` on Data
When you execute `docker rm`, the container instance and its top writable layer are permanently deleted. Any files created, modified, or stored inside the container during its execution—unless written to a persistent Docker Volume or Bind Mount—are permanently lost. This reinforces the cloud-native concept of containers being ephemeral (stateless and disposable).

### 4. DevOps Transformation through Containerization
Containerization solves the classic "it works on my machine" dilemma by packaging application code, libraries, and dependencies into an immutable container image. Developers can build and test exact replicas of the production environment locally. Operations teams can then deploy these identical containers across staging and production without worrying about environment mismatches, greatly accelerating CI/CD pipelines, automated testing, and collaborative deployments.

### 5. Evolution of GitHub Cloud Portfolio
My GitHub Cloud Computing portfolio is progressing from theoretical concepts toward hands-on cloud engineering skills. Adding structured lab activities with code snippets, terminal logs, and screenshot evidence demonstrates practical competence with tools like Docker and Linux environments. Organised documentation across distinct folders reflects professional cloud engineering standards.
