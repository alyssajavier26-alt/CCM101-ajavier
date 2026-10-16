# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/cloud-16.svg" width="28" height="28" />  The Cloud Operations Engineer

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/info-16.svg" width="20" height="20" /> Mission Overview
As a member of the Cloud Operations Team (Site Reliability Engineering) at CloudNova Technologies, this laboratory establishes performance baselines, deploys containerized applications, generates simulated web traffic, and tracks real-time metrics and application logs to ensure production readiness.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/goal-16.svg" width="20" height="20" /> Objectives
- Utilize native Linux command-line tools to monitor host CPU, Memory, and Disk capacity.
- Deploy a web container (`client-website`) and track its real-time performance using Docker metrics.
- Generate simulated web traffic and extract application access logs for troubleshooting.
- Translate raw performance data and container logs into readable Markdown technical documentation.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/terminal-16.svg" width="20" height="20" /> Monitoring Commands Executed
- **Host RAM Check:** `free -h`
- **Host Disk Capacity Check:** `df -h /`
- **Host Process Monitor:** `top`
- **Container Deployment:** `docker run -d --name client-website -p 8080:80 nginx:latest`
- **Traffic Generation:** `curl http://localhost:8080` & `curl http://localhost:8080/hidden-admin-page`
- **Log Extraction:** `docker logs client-website`
- **Container Metrics:** `docker stats`

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/cpu-16.svg" width="20" height="20" /> Skills Learned
- Establishing host system baselines and hardware capacity checks.
- Docker container deployment, log inspection, and real-time metric tracking.
- Translating raw terminal telemetry and HTTP logs into structured observability reports.
