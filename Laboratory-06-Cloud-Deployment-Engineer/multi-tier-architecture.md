# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/server-16.svg" width="28" height="28" /> Multi-Tier Architecture Research

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/info-16.svg" width="20" height="20" /> What is a Two-Tier Architecture?

A **Two-Tier Architecture** is a software design pattern where an application is split into two distinct, communicating functional layers or tiers: the **Web/Application Tier** (client interface and request processing) and the **Database Tier** (data storage, persistence, and management). In cloud containerization, these tiers run as separate, isolated containers linked together over a secure internal Docker network, enabling modular scalability and independent maintenance.

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/cpu-16.svg" width="20" height="20" /> The Web / Application Tier
* **Role:** Serves as the front-end interface that directly interacts with users. It handles incoming HTTP requests, processes application logic, renders web pages, and communicates user queries to the backend database.
* **Technology Example:** Nextcloud web application container (`nextcloud`).

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/database-16.svg" width="20" height="20" /> The Database Tier
* **Role:** Acts as the backend storage layer responsible for safely storing persistent data, user accounts, metadata, system configurations, and transactional records. It processes queries sent exclusively from the application tier.
* **Technology Example:** MariaDB relational database container (`mariadb:10.6`).

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/light-bulb-16.svg" width="20" height="20" /> Why Separate Them?

Separating the web server and the database into two distinct containers rather than packing them both into a single container is a core tenet of cloud-native design because it enforces separation of concerns and modular isolation. If both tiers resided in a single container, updating the web application or scaling traffic would risk corrupting database storage and violating container lifecycle best practices. Furthermore, a decoupled architecture allows administrators to scale, back up, secure, or reboot the web front-end independently without interrupting persistent backend data integrity.
