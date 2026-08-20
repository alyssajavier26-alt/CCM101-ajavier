# ☁️ Checkpoint 3: Identify Cloud Infrastructure Components

> **Laboratory Activity 2:** Build the Cloud Infrastructure Blueprint  
> **Course:** CCM101 - Cloud Infrastructure and Technologies  

---

## 📸 Component Architecture Overview

Modern cloud infrastructure relies on five core interconnected layers:

1. **Applications & Services** (Top Layer)
2. **Compute Resources** (*Virtual Machines, Containers, Serverless*)
3. **Storage & Networking Resources** (*Object/Block/File Storage, VPCs, Load Balancers*)
4. **Identity and Access Management** (*IAM, Authentication, RBAC*)
5. **Physical Infrastructure** (*Data Centers, Regions, Availability Zones*)

---

## 🛠️ Core Cloud Infrastructure Breakdown

### 1. ⚡ Compute Resources
Compute resources deliver the processing power (CPU and RAM) needed to execute software applications and workloads.

| Compute Type | Description | Key Characteristics | Industry Examples |
| :--- | :--- | :--- | :--- |
| **Virtual Machines (VMs)** | Emulated physical systems running full operating systems. | Strong resource isolation, complete OS control. | AWS EC2, Azure VMs, GCP Compute Engine |
| **Containers** | Lightweight environments sharing the host OS kernel. | Fast boot times, low resource overhead, high portability. | Docker, Kubernetes, OpenShift |
| **Serverless Computing** | Event-driven compute model running code on demand. | Zero infrastructure management, pay-per-execution model. | AWS Lambda, Azure Functions, Cloud Functions |

---

### 2. 💾 Storage Resources
Cloud storage provides secure, scalable locations for files, databases, and application data across redundant facilities.

* **📦 Object Storage:** Stores unstructured data like images, videos, backups, and static content.
  * *Examples:* Amazon S3, Azure Blob Storage, Google Cloud Storage
* **🧱 Block Storage:** Direct high-speed storage formatted as virtual hard drives for databases and VM disks.
  * *Examples:* Amazon EBS, Azure Managed Disks, GCP Persistent Disk
* **📁 File Storage:** Shared network file systems accessible by multiple virtual instances simultaneously.
  * *Examples:* Amazon EFS, Azure Files, Google Cloud Filestore

---

### 3. 🌐 Networking Resources
Networking connects virtual servers, databases, internet services, and users securely.

> 💡 **Key Network Services:**
> * **Virtual Private Cloud (VPC) / VNet:** Isolated virtual networks in the cloud.
> * **Load Balancers:** Distribute incoming traffic across instances for stability and uptime.
> * **Firewalls & Security Groups:** Control inbound and outbound network access rules.
> * **VPN Gateways:** Encrypted connections between local networks and cloud resources.

---

### 4. 🔐 Identity and Access Management (IAM)
IAM secures resources by managing authentication and authorization across the organization.

* **Principle of Least Privilege:** Users receive only the minimum permissions necessary for their tasks.
* **Authentication & Authorization:** Verifies identities and grants granular access permissions.
* **Role-Based Access Control (RBAC):** Assigns permissions based on defined organizational roles.
* **Multi-Factor Authentication (MFA):** Requires extra verification steps for secure login access.

---

### 5. 🌍 Physical Infrastructure: Regions & Availability Zones
The foundational physical sites hosting virtualized cloud infrastructure.

* **Data Center:** Physical facility housing servers, power supplies, cooling, and networking equipment.
* **Availability Zone (AZ):** One or more isolated data centers within a region with independent power and cooling.
* **Region:** Geographic location containing multiple interconnected Availability Zones to ensure high availability.
