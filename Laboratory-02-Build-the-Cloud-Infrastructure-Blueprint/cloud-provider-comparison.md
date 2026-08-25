
# Cloud Provider Comparison

## Introduction

Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP) are three of the most commonly used cloud platforms. Although each provider has its own service names, dashboard, and features, they all provide similar basic resources needed to build cloud-based systems. This comparison looks at their **compute, storage, networking, and identity and access management** services.

## Comparison of Major Cloud Services

| Component                        | AWS                                                                                                      | Microsoft Azure                                                                                                                  | Google Cloud                                                                                                        |
| -------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **Compute**                      | **Amazon EC2** – Allows users to create and manage virtual servers for applications and other workloads. | **Azure Virtual Machines** – Provides virtual computers that can run different operating systems and applications.               | **Compute Engine** – Offers customizable virtual machines for hosting applications and processing workloads.        |
| **Storage**                      | **Amazon S3** – Stores files, backups, application data, and other objects in the cloud.                 | **Azure Blob Storage** – Provides storage for large amounts of unstructured data such as documents, images, and videos.          | **Cloud Storage** – Stores data as objects inside cloud storage buckets.                                            |
| **Networking**                   | **Amazon VPC** – Creates a private and isolated network for AWS resources.                               | **Azure Virtual Network (VNet)** – Connects Azure resources through a private virtual network.                                   | **Google Cloud VPC** – Provides networking features such as subnets, IP addresses, and routing for cloud resources. |
| **Identity & Access Management** | **AWS IAM** – Manages users, roles, policies, and permissions for AWS resources.                         | **Microsoft Entra ID + Azure RBAC** – Handles identities and determines what users are allowed to access through assigned roles. | **Cloud IAM** – Controls access to Google Cloud resources using identities, roles, and permissions.                 |

The names of the services may differ, but their purposes are very similar. For example, **EC2, Azure Virtual Machines, and Compute Engine** all provide virtual computing resources. Likewise, **S3, Blob Storage, and Cloud Storage** are designed to store data in the cloud.

---

## Guide Questions

### 1. Which cloud provider offers the broadest range of services?

Among the three providers, **AWS** is commonly recognized for having one of the largest and most extensive collections of cloud services. It provides services for computing, databases, storage, networking, security, analytics, containers, artificial intelligence, and many other technologies. Its large selection makes it suitable for organizations with different types of cloud requirements.

### 2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products? Why?

For an organization that already relies heavily on Microsoft products, I would recommend **Microsoft Azure**. Azure works well with Microsoft's existing technologies and services, making it easier for organizations to connect their current systems with cloud-based resources. Its integration with Microsoft identity and business tools can also simplify account and access management.

### 3. Which platform is widely recognized for Artificial Intelligence, Machine Learning, and Kubernetes services?

**Google Cloud Platform (GCP)** is widely known for its capabilities in **Artificial Intelligence, Machine Learning, and Kubernetes**. Google has significant experience with these technologies, and its cloud services provide tools for developing, training, deploying, and managing AI and container-based applications.

### 4. What similarities did you observe among the three cloud providers?

The main similarity is that all three platforms provide the same fundamental building blocks for cloud infrastructure. Each provider has services for **computing, data storage, networking, and managing user access**. The biggest difference is usually the service name, interface, pricing structure, and specific features offered by each provider.

---

## Conclusion

AWS, Azure, and GCP may have different service names and management platforms, but their basic cloud concepts are largely the same. Each provider allows users to create virtual computing resources, store information, connect resources through networks, and control access using identity and permission systems. Learning these common concepts is useful because the knowledge can be applied when working with different cloud platforms.

## Official Documentation

* **AWS:** EC2, S3, VPC, and IAM
* **Microsoft Azure:** Virtual Machines, Blob Storage, Virtual Network, and Microsoft Entra ID
* **Google Cloud:** Compute Engine, Cloud Storage, VPC, and Cloud IAM
