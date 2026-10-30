# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/terminal-16.svg" width="28" height="28" /> Laboratory 09: The Cloud Automation Engineer

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/info-16.svg" width="20" height="20" /> Mission Overview
As a member of the Cloud Automation and DevOps Team at CloudNova Technologies, this laboratory eliminates human error by writing a Bash automation script to compress and back up critical client application data, modifying file permissions, and scheduling automated execution using the Linux Cron scheduler.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/goal-16.svg" width="20" height="20" /> Objectives
- Understand the fundamental syntax of a Bash shell script, including variables and basic commands.
- Use a command-line text editor (`nano`) to write and save executable scripts.
- Modify Linux file permissions using the `chmod` command.
- Understand task scheduling and the syntax of a Linux crontab.
- Document automation code and Cron job configurations using Markdown.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/terminal-16.svg" width="20" height="20" /> Commands Executed
- **Directory Creation:** `mkdir app-data`
- **Script Creation & Editing:** `nano backup.sh`
- **Permission Modification:** `chmod +x backup.sh`
- **Manual Execution:** `./backup.sh`
- **Backup Verification:** `ls -l backups/`
- **Cron Management:** `crontab -l` & `env EDITOR=nano crontab -e`

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/cpu-16.svg" width="20" height="20" /> Skills Learned
- Writing and structuring Bash shell scripts for infrastructure automation.
- Managing Linux file execution permissions and directory structures.
- Configuring automated time-based tasks using the Linux Cron scheduler.
- Translating DevOps automation workflows into clear Markdown technical documentation.
