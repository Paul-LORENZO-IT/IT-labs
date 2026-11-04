## 🛡️ Lab 01 – Linux Hardening & Access Control

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



## 📌 01. Project Overview

This project focuses on implementing an enterprise security baseline on Ubuntu Server 24.04 LTS.

The lab simulates a corporate multi-user environment where different departments share a centralized Linux server while maintaining strict access restrictions and controlled administrative privileges.

The main objective is to strengthen server security through:

Operating system hardening
Network protection
Identity and Access Management (IAM)
Filesystem permissions
Privilege management
Security auditing
Core Security Principle: Least Privilege

Every user should have access only to the resources and administrative operations required for their responsibilities.

# 🎯 02.Project Objectives

Security Domain	Implementation
SSH Security	SSH key authentication and root login restriction
Firewall	UFW firewall configuration
Intrusion Prevention	Fail2ban brute-force protection
Security Updates	Automated security updates
Identity Management	Linux users and groups
Access Control	POSIX ACLs
Privilege Management	Restricted sudo permissions
Security Auditing	Auditd monitoring

# 🏗️ 03. Infrastructure & Technologies
Lab Environment
Component	Configuration
Operating System	Ubuntu Server 24.04 LTS
Virtualization	VirtualBox / VMware
RAM	2–4 GB
CPU	2 vCPUs
Storage	25 GB
Network	NAT / Bridged Adapter
Security Technologies
Technology	Purpose
OpenSSH	Secure remote administration
UFW	Network firewall
Fail2ban	Brute-force prevention
Unattended Upgrades	Automated security patching
Linux Groups	Department-based access
POSIX ACLs	Granular filesystem permissions
Sudo	Administrative privilege delegation
Auditd	Security event monitoring

# 👥 04. Corporate User Structure

The lab simulates a corporate organization with three departments.

Department	Linux Group	User Account
IT Administration	it-admins	admin01
Human Resources	hr-team	hr01
Finance	finance-team	finance01
Shared Directory Architecture
text
/srv/company/
│
├── IT/
├── HR/
└── Finance/
Each department receives access only to its authorized workspace through Linux group permissions and POSIX ACLs.


# 🔐 05. Security Implementation

The project is divided into nine implementation phases.

Phase	Security Implementation	Tool
01	Initial Server Configuration	Ubuntu Server
02	SSH Hardening	OpenSSH
03	Firewall Configuration	UFW
04	Brute-Force Protection	Fail2ban
05	Automated Security Updates	Unattended Upgrades
06	User & Group Management	Linux IAM
07	Filesystem Access Control	POSIX ACLs
08	Privilege Delegation	Sudo
09	Security Monitoring	Auditd


# 🧪 06. Security Validation

Each security control will be tested to verify its effectiveness.

Security Test	Expected Result
Root SSH login	Denied
SSH password authentication	Disabled
SSH key authentication	Successful
UFW firewall	Active
Fail2ban service	Running
Department group membership	Verified
Unauthorized directory access	Denied
Authorized sudo command	Allowed
Audit rules	Loaded
📸 07. Evidence & Screenshots

Screenshots will document the implementation and validation of each security control.

Initial Ubuntu Server configuration
SSH hardening
UFW firewall rules
Fail2ban configuration
Automated security updates
User and group management
POSIX ACL permissions
Sudo privilege delegation
Auditd security monitoring

# 🧠 08. Skills Demonstrated
Linux System Administration
Ubuntu Server Hardening
SSH Security
Network Security
Firewall Management
Intrusion Prevention
Identity and Access Management (IAM)
Role-Based Access Control (RBAC)
POSIX ACLs
Privilege Management
Linux Security Auditing


# 🚀 09. Future Improvements
Centralized authentication with Active Directory or LDAP
Multi-Factor Authentication (MFA)
Centralized log management
Configuration automation with Ansible
Vulnerability scanning
Backup and disaster recovery
Security monitoring and alerting

# 📝 10. Conclusion
This lab demonstrates the practical implementation of a Linux server security baseline using Ubuntu Server 24.04 LTS.

By combining system hardening, network protection, identity management, filesystem permissions and administrative privilege controls, the project establishes a more secure and manageable multi-user environment.

Project Category: Linux Administration | Cybersecurity | IAM | Server Hardening

Platform: Ubuntu Server 24.04 LTS
