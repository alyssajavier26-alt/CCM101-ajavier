# ENTERPRISE CLOUD ARCHITECTURE
## Laboratory 10: Multi-Tier Containerized Web Service Cluster

An industrial-grade, highly secure infrastructure deployment engineering project establishing production-ready network isolation, persistent database storage, and automated backup routines.

### Executive Summary & Project Intent

Modern enterprise infrastructure requires rigorous decoupling between public-facing application layers and sensitive transactional data stores. Within this project workspace, an enterprise-class WordPress and MySQL cluster is fully containerized and orchestrated inside a localized Ubuntu Server operational environment.

By enforcing strict access control boundaries through custom bridge networking and persistent volume mapping, this deployment eliminates single-point-of-failure risks, protects database credentials from public exposure, and guarantees state preservation across continuous application lifecycles.

### Detailed System Architecture & Network Topology

The architecture establishes an isolated internal network space (`enterprise_net`) where the application tier acts as the sole gateway to backend database transactions. External traffic is filtered through a designated host port mapping directly to the CMS engine.

```text
                      +---------------------------------------+
                      |         Host Operations Stack         |
                      |   (Ubuntu Server / Bridged Adapter)   |
                      +-------------------+-------------------+
                                          |
                                          | Host Port Mapping: 8080 -> 80
                                          v
                      +-------------------+-------------------+
                      |      enterprise_wordpress_app         |
                      |        (PHP / Apache Engine)          |
                      +-------------------+-------------------+
                                          |
                                          | Internal Bridge Network: enterprise_net
                                          v
                      +-------------------+-------------------+
                      |        enterprise_mysql_db            |
                      |       (Relational Database)           |
                      +-------------------+-------------------+
                                          |
                                          | Persistent Volume Binding
                                          v
                      [ Host-Mounted Storage Volumes & Backups ]
```

### Comprehensive Component Breakdown

| **Tier / Service** | **Container Name** | **Core Responsibility** | **Network Exposure** | **Storage & Data Persistence** |
|---|---|---|---|---|
| **Front-End Layer** | `enterprise_wordpress_app` | Processes HTTP requests, executes core CMS logic, and serves theme assets. | Public Port: `8080:80` | Bind-mounted application folders for theme/plugin adjustments. |
| **Data Tier** | `enterprise_mysql_db` | Handles relational table schemas, user authentication credentials, and post states. | Internal Only (`3306`) | Isolated named Docker volume (`db_data`) mapped to `/var/lib/mysql`. |

### Directory Structure

```text
CCM101-ajavier/
└── Laboratory-10-Enterprise-Cloud-Architect/
    ├── README.md
    ├── architecture-diagram.png
    ├── docker-compose.yml
    ├── automation-script.sh
    ├── backup-wordpress.sh
    ├── operational-manual.md
    └── final-reflection.md
```

