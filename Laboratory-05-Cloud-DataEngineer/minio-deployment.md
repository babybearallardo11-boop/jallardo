# MinIO Deployment Documentation

## 1. Deployment Overview

This document describes the deployment of a MinIO object storage server using Docker. MinIO provides S3-compatible object storage that allows users to create buckets and store files through a web-based console.

## 2. Docker Command Used

The following command deploys the MinIO server in a Docker container:

```bash
docker run -d \
  --name minio-server \
  -p 9000:9000 \
  -p 9001:9001 \
  -e "MINIO_ROOT_USER=minioadmin" \
  -e "MINIO_ROOT_PASSWORD=minioadmin123" \
  quay.io/minio/minio server /data --console-address ":9001"
```

### Command Explanation

| Command or Flag | Purpose |
|---|---|
| `docker run -d` | Starts the container in the background. |
| `--name minio-server` | Assigns the container the name `minio-server`. |
| `-p 9000:9000` | Maps host port 9000 to the MinIO API port. |
| `-p 9001:9001` | Maps host port 9001 to the MinIO web console. |
| `-e "MINIO_ROOT_USER=minioadmin"` | Sets the administrator username through an environment variable. |
| `-e "MINIO_ROOT_PASSWORD=minioadmin123"` | Sets the administrator password through an environment variable. |
| `quay.io/minio/minio` | Specifies the MinIO container image. |
| `server /data` | Starts MinIO and uses `/data` as its storage directory inside the container. |
| `--console-address ":9001"` | Configures the web console to listen on port 9001. |

## 3. Web Console Access

The MinIO web console uses port **9001**.

- **Web Console:** http://localhost:9001
- **S3 API Endpoint:** http://localhost:9000

The console provides an interface for managing buckets, uploading files, and viewing stored objects.

## 4. Environment Variables (`-e` Flags)

The `-e` flag passes environment variables into the Docker container. In this deployment, the variables configure the credentials used to sign in to the MinIO administrator interface.

- `MINIO_ROOT_USER` defines the root username.
- `MINIO_ROOT_PASSWORD` defines the root password.

These variables allow MinIO to initialize its administrator credentials when the container starts. For a real deployment, strong credentials should be used instead of example values.

## 5. Bucket Creation

**Bucket Name:** `cloud-storage-bucket`

A bucket is a container used to organize objects, such as documents, images, and other files. The bucket was intended to demonstrate how MinIO stores and manages data using object storage.

> Replace `cloud-storage-bucket` with the actual bucket name you created during your laboratory activity.

## 6. Deployment Summary

The deployment demonstrates how Docker can run a MinIO object storage server and expose its services through mapped ports. Environment variables configure the administrator credentials, while the web console provides a convenient way to manage buckets and objects.
