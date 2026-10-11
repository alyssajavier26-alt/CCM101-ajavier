# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/file-code-16.svg" width="28" height="28" /> Docker Compose Technical Guide

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/info-16.svg" width="20" height="20" /> Infrastructure Architecture & YAML Explanations

#### 1. What does the `services:` block do?
The `services:` block defines the individual multi-container applications (or microservices) that make up the deployment stack. Each service under this block specifies its own container image, exposed ports, environment variables, and inter-service dependencies, allowing Docker Compose to manage them as a unified ecosystem.

#### 2. How did the Nextcloud app container find the database container?
The Nextcloud application container located the database container through the internal Docker bridge network using the **`MYSQL_HOST=database`** environment variable. Because Docker Compose automatically creates a custom bridge network for each project, containers can resolve each other using their defined service names (`database`) as hostnames.

#### 3. What is the difference between `docker run` and `docker-compose up -d`?
- **`docker run`**: A manual, single-container command where all parameters (ports, environment variables, network bindings, and image names) must be explicitly typed out every time. It is ideal for quick tests but cumbersome for multi-container apps.
- **`docker-compose up -d`**: An Infrastructure as Code (IaC) command that reads a declarative YAML configuration file (`docker-compose.yml`) to provision, link, and run multiple containers simultaneously in the background with a single command.
