# Laboratory 07: Cloud Operations Engineer

## Mission Overview
This laboratory focuses on monitoring a Linux host and observing a running Nginx Docker container. It demonstrates how system resources, container logs, and performance metrics help maintain a reliable cloud environment.

## Objectives
- Monitor the host's memory, disk, and CPU resources.
- Deploy an Nginx container using Docker.
- Test website availability through HTTP requests.
- Inspect container logs and identify HTTP errors.
- Monitor container CPU and memory usage.

## Monitoring Commands Executed
- `free -h` — checks memory information.
- `df -h /` — checks root disk capacity and usage.
- `top` — monitors running processes and CPU activity.
- `docker ps` — lists running containers.
- `curl` — tests website responses.
- `docker logs clientwebsite` — displays container logs.
- `docker stats clientwebsite` — monitors container resource usage.

## Skills Learned
I learned how to monitor Linux resources, deploy Docker containers, test HTTP responses, inspect logs, and observe container performance.

## Challenges Encountered
One challenge was understanding the information displayed by Linux monitoring commands. By examining the output and documenting the results, I improved my ability to identify system information and troubleshoot basic container issues.
