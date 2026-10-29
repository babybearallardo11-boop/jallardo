# Container Observability Report

## Container Deployment
- Container name: `clientwebsite`
- Container image: Nginx
- Port mapping: Host port `8080` to container port `80`
- Website URL: `http://localhost:8080/`

## HTTP Request Testing

The `curl` command was used to test the website and check its HTTP response status.

- First request status: [Enter actual status code]
- Second request status: [Enter actual status code]
- Third request status: [Enter actual status code]
- Nonexistent page tested: `/hidden-admin-page`
- Nonexistent page status: [Enter actual status code]

## Container Log Analysis

**Command:** `docker logs clientwebsite`

**Exact 404 log entry:**

[Paste the actual 404 log line from your terminal here.]

Container logs help administrators investigate requests and errors. They provide evidence that can be used to identify issues, such as a requested page that cannot be found.

## Container Resource Metrics

**Command:** `docker stats clientwebsite`

- CPU usage: [Enter actual CPU percentage]
- Memory usage: [Enter actual memory usage]
- Memory limit: [Enter actual memory limit]

Monitoring CPU and memory usage helps administrators understand how much of the host's resources the container consumes.

## Conclusion
Logs provide information about events and errors, while metrics show resource consumption and performance. Using both helps administrators monitor container health and troubleshoot application problems.
