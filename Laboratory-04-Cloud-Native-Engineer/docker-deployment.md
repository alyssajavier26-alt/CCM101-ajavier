# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/container-16.svg" width="28" height="28" /> The Container Lifecycle

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/terminal-16.svg" width="20" height="20" /> Container Lifecycle Commands

1. **`docker ps`**
   * *Explanation:* Lists all currently active and running containers along with their IDs, names, and port mappings.

2. **`docker stop my-nginx`**
   * *Explanation:* Gracefully stops the running container named `my-nginx` by sending a `SIGTERM` signal to its primary process.

3. **`docker ps -a`**
   * *Explanation:* Displays all containers on the host system, including active, paused, and exited/stopped containers.

4. **`docker rm my-nginx`**
   * *Explanation:* Permanently deletes the stopped `my-nginx` container instance and frees up system resource references.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/image-16.svg" width="20" height="20" /> Verification Evidence

![Container Lifecycle Execution](screenshots/container-lifecycle.png)
