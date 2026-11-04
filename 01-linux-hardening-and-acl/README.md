# 🛡️ Lab 01 – Linux Hardening & Access Control

## Project Overview

Enterprise Linux Server Hardening and Access Control using Ubuntu Server 24.04 LTS.

## Key Topics

- SSH Hardening
- UFW Firewall
- Fail2ban
- User and Group Management
- POSIX ACLs
- Sudo Privilege Management
- Security Auditing

## Documentation

Full implementation steps, configurations, security tests and screenshots.

🛡️ Ubuntu Server 24.04 LTS – Enterprise Hardening & Access Control

!Ubuntu !Security !Linux !Status
📌 Project Overview

This project demonstrates the implementation of an enterprise security baseline on Ubuntu Server 24.04 LTS.

The lab simulates a corporate multi-user environment where different departments share a centralized Linux server while maintaining strict access restrictions and controlled administrative privileges.

The main objective is to strengthen server security through system hardening, network protection, identity management, filesystem permissions, and security auditing.

Core principle: Principle of Least Privilege.

Every user should have access only to the resources and administrative operations required for their responsibilities.
🎯 Objectives

    Harden SSH authentication and disable direct root access.
    Configure UFW firewall rules.
    Deploy Fail2ban for SSH brute-force protection.
    Enable automated security updates.
    Implement department-based Linux user and group management.
    Configure POSIX ACLs for shared directories.
    Restrict administrative commands using sudo.
    Monitor security-related configuration changes using Auditd.

🏗️ Infrastructure
Component	Configuration
Operating System	Ubuntu Server 24.04 LTS
Virtualization	VirtualBox / VMware
RAM	2–4 GB
CPU	2 vCPUs
Storage	25 GB
Firewall	UFW
Intrusion Prevention	Fail2ban
Remote Access	OpenSSH
Access Control	Linux Groups and POSIX ACLs
Privilege Management	Sudo
Auditing	Auditd
🏢 Corporate User Structure
Department	Linux Group	User
IT Administration	it-admins	admin01
Human Resources	hr-team	hr01
Finance	finance-team	finance01

Each department receives a dedicated shared directory.
text

/srv/company/
│
├── IT/
├── HR/
└── Finance/

🔐 Security Implementation
1. SSH Hardening

    Disabled direct root login.
    Configured public-key authentication.
    Disabled password-based SSH authentication.
    Restricted SSH access to authorized accounts.
    Validated SSH daemon configuration.

2. Firewall Protection

Implemented UFW with a default-deny incoming policy.

    Restricted incoming connections.
    Authorized SSH access.
    Verified firewall rules.

3. Brute-Force Protection

Deployed Fail2ban to monitor SSH authentication attempts and temporarily ban IP addresses associated with repeated failures.
4. Automated Security Updates

Configured unattended-upgrades to automate security patch installation.
5. Identity and Access Management

Created dedicated Linux users and groups to simulate a corporate departmental structure.

Implemented role-based access control through Linux group membership.
6. POSIX ACLs

Configured granular permissions for departmental directories.

    IT users access IT resources.
    HR users access HR resources.
    Finance users access Finance resources.
    Unauthorized users are denied access.

7. Sudo Privilege Delegation

Configured dedicated sudoers policies to allow authorized administrative commands without granting unnecessary unrestricted root privileges.
8. Security Auditing

Configured Auditd to monitor changes to important identity and privilege configuration files.
🧪 Security Validation

The following controls were tested:
Test	Expected Result
SSH root login	Denied
SSH password authentication	Disabled
SSH key authentication	Successful
UFW status	Active
Fail2ban service	Running
Department group membership	Verified
HR access to Finance directory	Denied
Finance access to HR directory	Denied
Authorized sudo command	Allowed
Unauthorized sudo command	Denied
Audit rules	Loaded
📸 Evidence and Documentation

Screenshots are organized by implementation phase:

    Initial Ubuntu configuration.
    SSH hardening.
    Firewall and Fail2ban.
    Automated security updates.
    User and group management.
    POSIX ACL permissions.
    Sudo privilege delegation.
    Security auditing.

All screenshots represent practical validation performed in the Ubuntu virtual machine.
🧠 Skills Demonstrated

    Linux System Administration
    Ubuntu Server Hardening
    SSH Security
    Network Security
    Firewall Configuration
    Intrusion Prevention
    Identity and Access Management
    Role-Based Access Control
    POSIX ACLs
    Sudo Privilege Management
    Linux Security Auditing

🚀 Future Improvements

    Centralized authentication using LDAP.
    Multi-factor authentication.
    Centralized log management.
    Automated configuration management using Ansible.
    Vulnerability scanning.
    Backup and disaster recovery.
    Security monitoring and alerting.

📝 Conclusion

This project demonstrates practical Linux security administration skills through the implementation of multiple security controls on Ubuntu Server 24.04 LTS.

It establishes a secure foundation for a corporate multi-user environment by combining operating system hardening, network protection, identity management, filesystem access control, and privilege governance.

Project Category: Linux Administration | Cybersecurity | Server Hardening | IAM

Environment: Ubuntu Server 24.04 LTS
