# Checkpoint 2 – Research: Types of Cloud Storage

## Introduction

Cloud storage allows users and organizations to store, manage, and access data through cloud infrastructure. The three primary types of cloud storage are Block Storage, File Storage, and Object Storage. Each type has different features and is designed for specific storage requirements.

## Comparison of Cloud Storage Types

| Storage Type | Description (How It Stores Data) | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| **Block Storage** | Divides data into fixed-sized blocks, with each block stored separately and identified by a unique address. | Best for virtual machine disks, operating systems, and databases that require fast data access. | AWS Elastic Block Store (EBS) |
| **File Storage** | Organizes data into files and folders using a hierarchical directory structure. | Best for shared folders, document management, and applications that require multiple users to access the same files. | AWS Elastic File System (EFS) |
| **Object Storage** | Stores data as individual objects containing the data itself, metadata, and a unique identifier inside a storage bucket. | Best for user-uploaded images, videos, backups, documents, and other unstructured data. | AWS Simple Storage Service (S3) |

## Client Explanation: Why Object Storage Is the Best Choice

Object Storage is the best choice for storing user-uploaded images because it can handle large amounts of image files while providing reliable, scalable, and cost-effective storage. Each image is stored as an individual object that can be accessed through a unique identifier or URL, making it convenient for web and mobile applications. As the number of users and uploaded images grows, Object Storage can scale without requiring major changes to the storage infrastructure.

## Conclusion

Understanding the differences between Block Storage, File Storage, and Object Storage helps organizations choose the right solution for their needs. For a system that stores user-uploaded images, Object Storage offers an effective combination of scalability, accessibility, and cost efficiency.
