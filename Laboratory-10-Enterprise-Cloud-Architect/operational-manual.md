# Standard Operating Procedures & System Operations Manual

*System:* Enterprise Cloud Stack (WordPress + MySQL)  
*Host Environment:* Ubuntu Server 64-bit (Oracle VM VirtualBox)  
*Repository Path:* `~/CCM101-ajavier/Laboratory-10-Enterprise-Cloud-Architect`  

---

## Section 1: Network & Environment Baseline

### 1.1 Network Configuration
The host system uses Netplan for static IP assignment on the primary interface.
- *IP Address:* `192.168.1.58`
- *Subnet:* `/24` (`255.255.255.0`)
- *Gateway:* `192.168.1.1`

Verify network health:
```bash
ip addr show
ping -c 3 8.8.8.8
Section 2: Deployment & Service Management
To launch the enterprise multi-tier stack in detached mode:

Bash
docker compose up -d
To verify active container health and logs:

Bash
docker compose ps
docker logs enterprise_wordpress_app
