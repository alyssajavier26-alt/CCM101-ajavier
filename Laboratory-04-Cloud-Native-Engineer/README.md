# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/container-16.svg" width="28" height="28" /> Technical Documentation

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/info-16.svg" width="20" height="20" /> Mission Overview
Modern cloud computing relies heavily on lightweight, portable container technologies rather than traditional, resource-heavy Virtual Machines (VMs). In this mission for CloudNova Technologies, the objective is to demonstrate how containerization speeds up application delivery and optimizes resource consumption. Using the KillerCoda environment, we deployed, managed, and monitored a live Nginx web server using Docker CLI commands.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/goal-16.svg" width="20" height="20" /> Objectives
* Differentiate between traditional Virtual Machines (VMs) and process-isolated Containers.
* Access and utilize a Docker-enabled cloud environment using KillerCoda.
* Execute core Docker CLI commands to pull, run, inspect, and terminate containerized applications.
* Deploy a live Nginx web server and verify local HTTP responses via `curl`.
* Build comprehensive technical documentation and maintain a structured GitHub portfolio.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/terminal-16.svg" width="20" height="20" /> Docker Commands Executed

| Command | Purpose / Action |
| :--- | :--- |
| `docker --version` | Checks the currently installed Docker engine version. |
| `docker info` | Displays system-wide information regarding container counts and engine configuration. |
| `docker pull nginx` | Downloads the official Nginx base image from Docker Hub. |
| `docker run -d -p 8080:80 --name my-nginx nginx` | Launches an Nginx container in background mode, binding host port 8080 to container port 80. |
| `curl http://localhost:8080` | Sends a local HTTP request to verify the Nginx web server is serving traffic. |
| `docker ps` | Lists active, currently running containers. |
| `docker stop my-nginx` | Sends a termination signal to gracefully stop the running `my-nginx` container. |
| `docker ps -a` | Lists all containers on the host system, including stopped and exited instances. |
| `docker rm my-nginx` | Permanently removes the stopped `my-nginx` container instance. |

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/cpu-16.svg" width="20" height="20" /> Skills Learned
* **Container Lifecycle Management:** Practical experience in provisioning, inspecting, stopping, and removing container instances.
* **Port Mapping & Networking:** Understanding how host ports communicate with isolated container network ports (`-p 8080:80`).
* **Process vs. Hardware Isolation:** Hands-on realization of container efficiency compared to hypervisor-based virtualization.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/alert-16.svg" width="20" height="20" /> Challenges Encountered
* **Port Conflicts:** Ensuring port `8080` was free on the host environment before running the container run command.
* **Image Management:** Ensuring proper container removal (`docker rm`) before attempting to recreate containers with the same name tag.
