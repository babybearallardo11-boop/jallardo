# Mission 6 Reflection

Writing a `docker-compose.yml` file makes a cloud engineer's job easier because all the services and their configurations are organized in one place. Instead of starting every container separately, I can use one command to deploy the application stack. This makes the setup easier to repeat and document.

YAML indentation is important because it defines how configuration elements are organized. Incorrect spacing or tabs can cause parsing errors and prevent the application from starting correctly. This taught me to check the configuration carefully before deployment.

Environment variables such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_USER` provide configuration values to the containers. They help Nextcloud connect to MariaDB with matching settings. I also learned that passwords should not be exposed in public repositories and that secure credential management is important.

Deploying Nextcloud with MariaDB helped me understand how separate services work together to provide private cloud storage. Docker Compose reduced the number of manual steps and made the deployment process easier to understand.

Since Mission 1, my understanding of cloud computing has grown from learning basic Linux commands to understanding how applications, databases, containers, and networks work together. I have also learned that documentation and configuration files are important in infrastructure management. I still need more practice with security, persistent storage, and troubleshooting, but this mission has increased my confidence in using Linux and Docker.
