# Docker Compose Guide

## The services: Block
The `services:` block defines the containers used by the application. The `database` service runs MariaDB, while the `app` service runs Nextcloud.

## MYSQL_HOST
The `MYSQL_HOST=database` environment variable tells Nextcloud to connect to the service named `database`.

## Environment Variables
Environment variables configure database credentials and settings. Real deployments should use secure secrets management.

## Docker Run Versus Docker Compose
`docker run` commonly starts an individual container. `docker-compose up -d` starts the services defined in the Compose file in the background.

## Commands
- `docker-compose up -d` starts the services.
- `docker-compose ps` checks container status.
- `docker-compose down` stops and removes the containers and network.
