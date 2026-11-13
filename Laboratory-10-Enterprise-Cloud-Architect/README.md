# Enterprise Cloud Architect

## 1. System Overview & Architecture
- **Virtualization:** Oracle VM VirtualBox running Ubuntu Server 64-bit with the network adapter set to Bridged Adapter mode.
- **Networking:** Fixed Static IP configuration (`192.168.1.58/24`) managed via Netplan (`/etc/netplan/00-installer-config.yaml`).
- **Containerization:** Docker & Docker Compose orchestrating an enterprise WordPress web application tied to an isolated MySQL database container (`enterprise_mysqql_db`) with persistent storage volumes.
- **Automation:** Shell script automation for dynamic database backups, compression, and maintenance logs.

---

## 2. Directory Structure
```text
CCM101-ajavier/
└── Laboratory-10-Enterprise-Cloud-Architect/
    ├── README.md
    ├── docker-compose.yml
    ├── automation-script.sh
    ├── backup-wordpress.sh
    ├── operational-manual.md
    └── final-reflection.md
