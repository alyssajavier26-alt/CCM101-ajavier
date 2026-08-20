# ☁️ Technical Documentation

---

## 📌 Mission Overview
In this mission, CloudNova Technologies tasked our engineering team with investigating cloud infrastructure components within a cloud-hosted Linux environment prior to service deployment. This documentation serves as a comprehensive Cloud Infrastructure Assessment Report detailing the compute, storage, networking, operating system, and cloud provider resources necessary for architectural design.

---

## 🎯 Objectives
* Explain the major components of cloud infrastructure.
* Investigate hardware and software resources in a Linux server environment.
* Differentiate compute, storage, networking, and identity resources.
* Interpret relationships between cloud infrastructure components.
* Create professional technical documentation using structured Markdown.
* Design a fundamental cloud infrastructure diagram.
* Continue expanding the GitHub Cloud Computing Portfolio.

---

## 🛠️ Cloud Infrastructure Components
* ⚡ **Compute Resources:** Processing units (Virtual CPUs and RAM) responsible for handling operational computations and running application processes.
* 💾 **Storage Resources:** Persistent and non-persistent storage systems (Block and Object storage) used for retaining system binaries, databases, and application files.
* 🌐 **Networking Resources:** Virtual networks, subnets, IP addresses, and routing tables that enable secure communication between instances and external users.
* 🐧 **Operating System:** Standardized interface software (Ubuntu 24.04 LTS) managing hardware abstractions and software dependencies.

---

## 🧰 Tools Used
* **KillerCoda Playground:** Cloud-hosted Linux execution terminal.
* **Linux CLI Utilities:** Built-in shell diagnostics (`lscpu`, `free`, `df`, `ip`, `uname`).
* **Git & GitHub:** Version control and portfolio hosting.
* **Diagramming Tool:** Draw.io / Excalidraw for architecture visualization.
* **Markdown:** Technical documentation formatting.

---

## 🖥️ Linux Commands Executed

| Command | Purpose |
| :--- | :--- |
| `cat /etc/os-release` & `uname -r` | Inspected system distribution details and Linux kernel version. |
| `lscpu` | Examined CPU architecture model and virtual core availability. |
| `free -h` | Evaluated allocated physical RAM capacity and active usage. |
| `df -h` | Profiled mounted file system disk space and storage boundaries. |
| `hostname` & `ip addr` | Identified virtual hostname and internal IP networking configurations. |
| `mkdir -p` & `touch` | Constructed standardized documentation directory structures. |

---

## 🧠 Skills Learned
* Shell-based system profiling and cloud hardware assessment.
* Translating physical server resource metrics into cloud service components.
* Comparative mapping across major public cloud providers (AWS, Azure, GCP).
* Architectural diagramming for cloud networks, compute nodes, and user access flows.

---

## 💡 Challenges Encountered

> ⚠️ **Challenge:** Distinguishing private container IP interface routes from external host network adapters.  
> ✅ **Solution:** Used `ip addr` alongside `hostname` output analysis to pinpoint the internal loopback and primary virtual adapter bindings.
