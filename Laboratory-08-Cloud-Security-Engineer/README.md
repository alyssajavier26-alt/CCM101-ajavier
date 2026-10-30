# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/shield-16.svg" width="28" height="28" /> The Cloud Security Engineer

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/info-16.svg" width="20" height="20" /> Mission Overview
As a member of the elite Cloud Security Team at CloudNova Technologies, this laboratory implements defense-in-depth principles by locking down a live server using a host-based firewall, auditing open ports, and securing containerized applications against unauthorized access.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/goal-16.svg" width="20" height="20" /> Objectives
- Understand the concept of the Attack Surface and the Principle of Least Privilege (PoLP).
- Deploy a vulnerable Nginx web container (`secure-web-app`) and verify its reachability.
- Configure the Uncomplicated Firewall (UFW) with a strict Default Deny incoming policy.
- Implement granular port management to selectively allow SSH and HTTP traffic on port 8080.
- Document security configurations and firewall rules using Markdown.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/terminal-16.svg" width="20" height="20" /> Commands Executed
- **Container Deployment:** `docker run -d --name secure-web-app -p 8080:80 nginx:latest`
- **Allow SSH Access:** `sudo ufw allow ssh`
- **Default Deny Policy:** `sudo ufw default deny incoming` & `sudo ufw default allow outgoing`
- **Enable UFW:** `sudo ufw enable`
- **Allow Web Traffic:** `sudo ufw allow 8080/tcp`
- **Status Verification:** `sudo ufw status numbered` & `sudo ufw status verbose`
- **Traffic Testing:** `curl http://localhost:8080`

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/cpu-16.svg" width="20" height="20" /> Skills Learned
- Enforcing host-based security controls and foundational firewall policies.
- Managing inbound and outbound network traffic using UFW.
- Mitigating exposure risks through precise port management and attack surface reduction.
- Translating cloud security configurations into professional Markdown technical documentation.
