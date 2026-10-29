# Laboratory Reflection: Cloud Operations Engineer

In this laboratory, I learned that monitoring system resources is important in managing a cloud environment. Checking RAM helps me understand the available memory, while checking disk capacity helps prevent storage-related problems. Monitoring CPU usage is also useful because excessive resource consumption can affect application performance.

The `docker logs` command can help troubleshoot a website problem. For example, if a user reports that a page cannot be accessed, I can inspect the Nginx container logs to identify the request and its response. An HTTP 404 error usually means that the requested resource was not found. This information helps me investigate the issue instead of guessing its cause.

I also learned the difference between logs and metrics. Logs record events, requests, and errors, helping explain what happened. Metrics provide numerical information, such as CPU and memory usage, which helps administrators evaluate performance. Both are useful because metrics can reveal unusual resource consumption, while logs provide details about specific events.

When managing thousands of containers, monitoring tools such as Prometheus and Grafana can help organize system information. Prometheus collects metrics, while Grafana presents the data through dashboards. These tools make it easier for administrators to monitor trends, identify potential problems, and respond to alerts.

Overall, this activity improved my Linux troubleshooting skills. I became more familiar with checking system resources, testing website responses, examining Docker logs, and monitoring container performance. I realized that effective cloud operations requires patience, careful observation, and the use of actual system data when investigating problems.
