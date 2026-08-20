cat << 'EOF' > infrastructure-report.md
# Cloud Infrastructure Assessment Report

## Executive Summary
This report documents the technical specifications of the Linux instance running inside the KillerCoda cloud environment. All parameters were collected through direct command-line investigation.

---

## System Infrastructure Profile

| Specification | Technical Finding | Diagnostic Command |
| :--- | :--- | :--- |
| **Operating System** | Ubuntu 24.04.4 LTS (Noble Numbat) | `cat /etc/os-release` |
| **Kernel Version** | `6.8.0-138-generic` | `uname -r` |
| **CPU Model** | Intel Xeon E312xx (Sandy Bridge, IBRS update) @ 2.0GHz | `lscpu` |
| **Number of CPU Cores** | 1 Core (1 Thread per core, 1 Socket) | `lscpu` |
| **Total RAM** | 1.9 GiB (Used: 414 MiB, Available: 1.5 GiB) | `free -h` |
| **Disk Capacity** | 19 GiB Root Partition (`/dev/vda1`) | `df -h` |
| **Mounted File Systems** | `/dev/vda1` (`/`), `/dev/vda16` (`/boot`), `/dev/vda15` (`/boot/efi`), `tmpfs` (`/run`) | `df -h` |
| **Hostname** | `ubuntu` | `hostname` |
| **IP Address** | `172.30.1.2/24` (Interface: `enp1s0`), `172.17.0.1/16` (Docker) | `ip addr` |

---

## Detailed Component Analysis

### 1. Operating System & Kernel
* Distribution running is **Ubuntu 24.04.4 LTS** running on the long-term support Linux kernel `6.8.0-138-generic`.

### 2. Virtual Compute Architecture
* Single-core x86_64 CPU configuration (`Intel Xeon E312xx`) allocated under KVM full virtualization.
* Physical system memory total is 1.9 GiB with a 1.0 GiB swap allocation.

### 3. Storage & Partition Layout
* **Root Storage:** Block storage slice `/dev/vda1` provides 19 GiB total capacity with 13 GiB available.
* **System Partitions:** `/boot` mounted at `/dev/vda16` (881 MiB) and EFI boot sector mounted at `/dev/vda15` (105 MiB).

### 4. Network Configuration
* **Primary Adapter (`enp1s0`):** Configured with private IPv4 address `172.30.1.2/24`.
* **Container Interface (`docker0`):** Virtual bridge assigned to `172.17.0.1/16`.
