# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/shield-16.svg" width="28" height="28" /> Firewall Configuration & Security Guide

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/terminal-16.svg" width="20" height="20" /> UFW Security Commands Executed
- **Allow SSH Remote Access:** `sudo ufw allow ssh`
- **Set Default Deny Policy (Incoming):** `sudo ufw default deny incoming`
- **Set Default Allow Policy (Outgoing):** `sudo ufw default allow outgoing`
- **Enable Firewall:** `sudo ufw enable`
- **Allow Port 8080 (Web App):** `sudo ufw allow 8080/tcp`
- **Verify Numbered Rules:** `sudo ufw status numbered`

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/info-16.svg" width="20" height="20" /> Configuration Analysis

#### 1. The Role of `chmod +x`
*(Note: While file execution permissions apply to script execution rather than UFW rules directly, modifying file permissions ensures scripts and binaries execute correctly with proper user privilege controls.)*

#### 2. Risk of Enabling UFW Before Allowing SSH
If you ran `sudo ufw enable` before running `sudo ufw allow ssh`, the active firewall would immediately block all incoming connections on port 22, permanently locking you out of your remote SSH administration session.

#### 3. UFW Port 8080 Rule Breakdown
By explicitly running `sudo ufw allow 8080/tcp`, the host-based firewall permits inbound TCP traffic on port 8080, allowing external users and `curl` tests to reach the Nginx container (`secure-web-app`) while maintaining strict default-deny protection across all other unapproved ports.
