# 🗺️ Systems, Networks & IAM Learning Path

Hello! I am currently working toward my certification as a **Senior Systems and Networks Technician (TSSR)**. With a keen interest in access security, I am focusing my skills on **IAM (Identity and Access Management)**.

This portfolio outlines my technical journey through four major hands-on labs, covering everything from on-premises infrastructure to cloud governance and security.


## 🎯 Progress Roadmap

| # | Lab | Core Topic | Technologies & Tools | Status |
| :-: | :--- | :--- | :--- | :-: |
| **01** | **Linux Hardening & Local Access** | SSH key auth, UFW firewall, system permissions, Fail2ban | Ubuntu Server | 🟢 Done |
| **02** | **Centralized Identity (On-Prem)** | Active Directory, GPO security policies, DNS, DHCP | Windows Server | 🚧 In Progress |
| **03** | **Cloud IAM & Modern Auth** | Microsoft Entra ID, RBAC, Conditional Access, MFA | Entra ID / Azure | 📅 Planned |
| **04** | **Governance & Automation** | JML Lifecycle (Joiner/Mover/Leaver), Least Privilege | PowerShell / Bash, AWS IAM | 📅 Planned |

---

## 🛠️ Lab Details & Scenarios

### 🟢 Lab 01: Linux Hardening & Local Access Control
* **Scenario:** Secure a production Ubuntu Server against brute-force attacks and unauthorized access.
* **Key Achievements:**
  * Created a dedicated administration user and fully disabled `root` remote login.
  * Enforced asymmetric cryptography via **Ed25519 SSH keys** and blocked password authentication.
  * Secured the network perimeter using **UFW** (restricted ports, default deny).
  * Implemented proactive defense with **Fail2ban** to auto-ban malicious IPs.
* **[🔗 View Lab Documentation & Screenshots](./01-linux-hardening)**

### 🚧 Lab 02: Centralized Corporate Identity (Active Directory)
* **Scenario:** Design and build the core local IT infrastructure for a growing company of 50+ employees.
* **Key Achievements:**
  * Deploying a Windows Server Domain Controller (`corporate.local`) with proper OU nesting.
  * Implementing foundational network services: **DHCP scopes** and **DNS zones**.
  * Enforcing security Baselines via **Group Policies (GPOs)** (Password complexity, screen lockout, drive mapping).
* **[🔗 View Current Work](./02-active-directory)**

### 📅 Lab 03: Modern Identity & Hybrid Cloud (Entra ID)
* **Scenario:** Bridge the gap between On-Premises infrastructure and Cloud SaaS resources securely.
* **Target Objectives:**
  * Sync on-prem identities to the cloud using Microsoft Entra Connect.
  * Define strict **Conditional Access Policies** (e.g., blocking logins outside specific locations).
  * Configure **Multi-Factor Authentication (MFA)** and Role-Based Access Control (RBAC).

### 📅 Lab 04: Governance & JML Automation
* **Scenario:** Automate user lifecycle operations to reduce human error and eliminate orphaned accounts.
* **Target Objectives:**
  * Build a PowerShell/Bash engine automating **Joiner / Mover / Leaver (JML)** user states.
  * Map access requests directly to automated group memberships.
  * Implement Least Privilege principles through **AWS IAM** JSON policies.
