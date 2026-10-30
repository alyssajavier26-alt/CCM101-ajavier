# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/shield-16.svg" width="28" height="28" /> Security Audit Report & Best Practices

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/book-16.svg" width="20" height="20" /> Core Security Concepts

#### 1. The Principle of Least Privilege (PoLP)
The Principle of Least Privilege dictates that user accounts, processes, and systems should be granted only the absolute minimum permissions and access rights necessary to perform their specific functions. This security concept is critical for cloud user accounts because it drastically limits the potential "blast radius" if an account or credential is ever compromised, preventing attackers from gaining full administrative control over the entire environment.

#### 2. Attack Surface
An attack surface refers to the total sum of all vulnerable points, exposed network ports, running services, and entry vectors across a virtual machine or cloud infrastructure that an unauthorized user or malicious actor can try to access or exploit. Minimizing this surface by closing unused ports and disabling unnecessary services is essential for reducing overall security risk.

#### 3. Default Deny Policy
A Default Deny policy is a foundational security stance where all incoming network traffic is blocked by default, and access is only permitted through explicit, pre-approved rules. It is significantly safer than trying to block specific malicious hackers individually because malicious actors constantly change their IP addresses and attack methods, whereas a deny-all baseline ensures no unexpected entry points remain open.
