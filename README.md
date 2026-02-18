# System Hardening Ubuntu

This project focuses on hardening an Ubuntu system for a simulated company **Baker Street Inc.**, by appplying configurations, reducing the attack surface, and validating improvements through auditing and scanning. it demonstrates practical blue-teams skills aligned with real SOC and sysadmin workflows, including user auditing, SSH security, passoword policy enforcement, service reduction and logging configuration. 

A full technical brief with screenshots and detailed steps is included in this repository. 

# Objectives
- OS Backup
- Auditing groups and users
- Updating & enforcing password polcies
- Updating & enforcing sudo permissions
- Validating & updating permissions on files and directories
- Updating password hasing configuration
- Auditing & securing SSH
- Reviewing & updating system packages
- Disabling unnecessary services
- Creating and scheduling cron jobs

# Tools & Techologies
- **Ubuntu Linux**
- **Terminal / Bash**
- **UFW**
- **OpenSSH**
- **auditd**
- **cron**
- **Nmap**
- **tar**

# Key Hardening Steps
### 1. User & Group Auditing
- Reviewed all system users and groups
- Verified authorized sudo users
- Disabled or removed unnecessary accounts

### 2. Password & Authentication Policies
- Enforced password complexity and expiration
- Configured account lockout for failed attempts
- Updated PAM and login.defs for strong authentication

### 3. Sudo Permissions Hardening
- Restricted sudo access to authorized users
- Required password for all sudo actions
- Ensured sudo activity is logged

### 4. File & Directory Permission Validation
- Audited sensitive files (/etc/passwd, /etc/shadow, /etc/sudoers)
- Corrected permissions to prevent unauthorized access

### 5. SSH Hardening
- Disbabled root login
- Disabled password authentication
- Enforced key-based authentication
- Configured idle timeouts
- Reduced SSH attack surface through configuration changes

### 6. System Updates & Package Management
- Updated all system packages
- Removed outdated or unnecessary software
- Enabled automatic security updates

### 7. Service Reduction
- Identified running services
- Disabled services not required for system operation

### 8. Logging & Auditing
- Installed and configured **auditd**
- Enabled logging for authentication, privilege escalation, and system modifications

### 9. Scheduled Tasks
- Created cron jobs for log rotation, updates, and system checks

# Validation & Testing
To confirm the effectiveness of the hardening:

#### Nmap Scanning
- Performed scans before and after hardening
- Verified reduced open ports
- Confirmed disabled services were no longer accessible

#### Log Review
- Checked authentication logs
- Verified sudo activity logging
- Confirmed auditd rules were triggering correctly

# Project Artifacts 
The following files are included in this repository:
- **Full Technical Brief (PDF)** - Complete walkthrough with screenshots
- **Before/After Scan Results**
- **auditd Rules File**
- **Cron Job Configurations**
- **SSH Configuration Snippet**

# Lessons Learned
- Hardening is a layered process - no single change is enough and I can understand why change management is so important
- Logging is essential for visibility and incident response
- SSH misconfigurations can lock you out if not tested carefully
- Principle of least privilege dramatically reduces risk
- Auotmation helps maintain long-term security posture

# Summary
This project demonstrates my ability to audit, secure, and validate a Linux system using real-world defensive techniques. It reflects the same workflows used in SOC, sysadmin, and blue team environmens and showcases my attention to detail, curiosity, and commitment to doing thing correctly.

