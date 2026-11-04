# 🛡️ Lab 01 – Linux Hardening & Access Control

An enterprise security baseline implementation on **Ubuntu Server 24.04 LTS**. This project simulates a corporate multi-user environment where distinct departments share a centralized Linux infrastructure while enforcing strict zero-trust boundary controls, granular filesystem segregation, and comprehensive security auditing.

---

## 📌 01. Project Overview

This deployment establishes a production-hardened Linux server architecture by implementing defense-in-depth methodologies. The lab focuses on minimizing attack surfaces, governing multi-tenant computational spaces, and auditing system state changes.

### ⚖️ Core Security Principle: Least Privilege
> **Every system identity, group, and process is restricted exclusively to the minimal computational resources and cryptographic privileges required to execute its explicit responsibilities.**

---

## 🎯 02. Project Objectives

| Security Domain | Operational Implementation |
| :--- | :--- |
| **SSH Cryptography** | Enforce asymmetric public-key handshakes and absolute administrative connection drops. |
| **Network Protection** | Deploy stateful packet filtering via an implicit default-deny network firewall. |
| **Intrusion Prevention** | Monitor live log structures to dynamically block brute-force vectors. |
| **Patch Management** | Automate immediate mitigation of CVEs via headless security package patching. |
| **Identity Governance** | Establish role-based user/group directory access mapping corporate topology. |
| **Access Control** | Bypass static standard UNIX bits using granular POSIX Access Control Lists (ACLs). |
| **Privilege Governance** | Restrict, decouple, and delegate specific sub-administrative operational entitlements. |
| **Continuous Auditing** | Track kernel system calls and critical security events in a tamper-resistant daemon. |

---

## 🏗️ 03. Infrastructure & Technologies

### 💻 Virtualization & Hardware Allocation
*   **Operating System:** Ubuntu Server 24.04 LTS
*   **Hypervisor Compatibility:** VMware Workstation / Oracle VirtualBox
*   **Compute:** 2 vCPUs
*   **Memory:** 2 GB – 4 GB RAM
*   **Storage:** 25 GB Virtual Disk Space
*   **Networking:** NAT / Bridged Adapter mapping

### 🛠️ Core Security Stack
*   **OpenSSH Engine:** Encapsulated remote session handling and access control.
*   **Netfilter / UFW:** Stateful host-level kernel network traffic control.
*   **Fail2ban Daemon:** Automated log analysis and real-time host interdiction.
*   **Unattended-Upgrades:** Non-interactive autonomous security package management.
*   **POSIX ACLs (`linux-apps/acl`):** Multi-entity modern permission mapping.
*   **Sudo Engine:** Granular privilege escalation delegation.
*   **Auditd Framework:** Kernel-level telemetry, tracking, and system compliance logging.

---

## 👥 04. Corporate User Structure

The infrastructure organizes three separate corporate entities into isolated operational environments.

### 🏢 Directory Architecture
```text
/srv/company/
├── IT/       (it-admins exclusive write access)
├── HR/       (hr-team exclusive write access)
└── Finance/  (finance-team exclusive write access)
```

### 👤 Identity Matrix
*   **IT Administration**
    *   *System Group:* `it-admins`
    *   *Assigned Account:* `admin01`
*   **Human Resources**
    *   *System Group:* `hr-team`
    *   *Assigned Account:* `hr01`
*   **Finance Department**
    *   *System Group:* `finance-team`
    *   *Assigned Account:* `finance01`

---

## 🔐 05. Security Implementation Matrix

The lab deployment executes systematically across nine specific phases:

Use code with caution.
┌─────────────────────────────────────────────────────────────────────────┐
│  01. Initial Server Prep ──► 02. OpenSSH Hardening ──► 03. UFW Firewall  │
└─────────────────────────────────────────────────────────────────────────┘
│
┌─────────────────────────────────────────────────────────────────────────┐
│  06. IAM Group Provision ◄── 05. Security Updates  ◄── 04. Fail2ban     │
└─────────────────────────────────────────────────────────────────────────┘
│
┌─────────────────────────────────────────────────────────────────────────┐
│  07. POSIX ACL Locking   ──► 08. Sudo Delegation  ──► 09. Auditd Logs   │
└─────────────────────────────────────────────────────────────────────────┘

---

## 🧪 06. Security Validation Framework

| Target Mechanism | Operational Vector | Expected Security Result |
| :--- | :--- | :--- |
| **SSH Integrity** | Remote root login attempt | **Explicitly Denied** |
| **Credential Lock** | Password-based authentication handshake | **Explicitly Denied** |
| **Identity Proof** | Authorized private key submission | **Successful Handshake** |
| **Network Border** | Stateful packet monitoring check | **Active / Enforcing** |
| **Dynamic Block** | Repetitive failure threshold breaches | **Automated IP Drop** |
| **IAM Isolation** | Out-of-bounds cross-department navigation | **Permission Denied** |
| **Sudo Restriction** | Non-authorized privilege escalation request | **Operational Refusal** |
| **Telemetry State** | Live monitoring check (`auditctl -l`) | **Audit Rules Loaded** |

---

## 📸 07. Evidence & Screenshots Index
*(Maintain exact visual captures inside the `/assets/screenshots/` workspace to serve as verifiable project proof)*

1.  **Initial Infrastructure Setup:** `01_base_ubuntu_install.png`
2.  **SSH Hardening Verification:** `02_ssh_hardened_config.png`
3.  **Firewall Rules Status:** `03_ufw_status_verbose.png`
4.  **Fail2ban Prison Status:** `04_fail2ban_jail_status.png`
5.  **Autonomous Update Configuration:** `05_unattended_upgrades_log.png`
6.  **Corporate User Matrix:** `06_user_group_id_matrix.png`
7.  **POSIX Advanced Permissions:** `07_getfacl_directory_output.png`
8.  **Sudoers Policy Enforcement:** `08_sudo_privilege_test.png`
9.  **Auditd Security Telemetry:** `09_auditd_log_generation.png`

---

## 🧠 08. Core Skills Demonstrated

*   Enterprise Linux Systems Engineering (Ubuntu Server 24.04 LTS Architecture)
*   Asymmetric Cryptography Deployment & SSH Key Management
*   Host-Level Network Architecture & Kernel Firewall Provisioning
*   Proactive Threat Interdiction & Log Ingestion Engineering
*   Role-Based Identity Governance & Access Management (RBAC)
*   Advanced POSIX Access Control Matrix Design (`getfacl` / `setfacl`)
*   Secure Privilege Separation Policies & System Call Event Tracking

---

## 🚀 09. Future Architectural Roadmap

*   **Identity Federation:** Migration to centralized directory domains via Microsoft Active Directory or OpenLDAP.
*   **Multi-Factor Handshakes:** Implementation of Pluggable Authentication Modules (PAM) for MFA via Google Authenticator.
*   **Log Management:** Ingestion of infrastructure logs into a centralized SIEM instance (Wazuh / Elastic Stack).
*   **Infrastructure-as-Code:** Packaging the configuration matrices into automated Ansible Playbooks.
*   **Continuous Backups:** Automated point-in-time state backups via customized rsync cron scheduling.

---

## 📝 10. Conclusion

This deployment successfully establishes a modern, multi-user Linux environment secure enough for real-world enterprise operations. By stripping down standard weaknesses and reinforcing every level of the OS, the system provides strong system compliance, absolute operational boundaries, and complete administrative transparency.

***

**Project Category:** Linux Systems Administration | Cybersecurity Engineering | Host-Level Hardening | Identity & Access Management (IAM)
**Platform Baseline:** Ubuntu Server 24.04 LTS Productive Kernel
