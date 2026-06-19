# Help-Desk-Lab
# Enterprise Active Directory Home Lab

## Overview

This project simulates a small enterprise Windows environment using Windows Server 2022, Active Directory Domain Services (AD DS), Group Policy, and role-based access controls.

The objective was to gain hands-on experience with the technologies and administrative tasks commonly performed by Help Desk Technicians, Systems Administrators, and IT Support Specialists.

---

## Environment

### Infrastructure

* Windows Server 2022
* Active Directory Domain Services (AD DS)
* DNS
* VirtualBox

### Domain

* Vance.com

### Domain Controller

* OH-DC-01

---

## Organizational Structure

The Active Directory environment was designed to simulate a real organization with departmental separation through Organizational Units (OUs).

### Departments

* Executives
* IT
* HR
* Finance
* Sales
* Operations

---

## User and Identity Management

Created and managed user accounts across multiple departments.

### Example Users

#### IT

* Emily Brown – Help Desk Technician
* David Carter – System Administrator
* Michael Lee – IT Manager

#### HR

* Sarah Johnson – HR Specialist
* Jessica Miller – HR Manager

#### Finance

* Amanda Davis – Finance Manager
* Robert Wilson – Accountant

#### Sales

* John Smith – Sales Representative
* Chris Taylor – Sales Representative
* Kevin White – Sales Manager

#### Operations

* Brian Moore – Operations Manager
* Mark Anderson – Operations Coordinator

#### Executives

* Jennifer Winters – CEO
* Thomas Harris – COO

---

## Security Groups

Implemented role-based access control (RBAC) using Active Directory Security Groups.

### Groups

* IT_Admins
* HR_Users
* Finance_Users
* Sales_Users
* Operations_Users
* Executives

Users were assigned permissions through security groups rather than individually, following enterprise best practices.

---

## Shared File Infrastructure

Created departmental shared folders:

```text
C:\Shares

├── Executives
├── Finance
├── HR
├── IT
├── Operations
├── Sales
└── Public
```

### Access Controls

Configured NTFS permissions using security groups:

* HR_Users → HR Share
* Finance_Users → Finance Share
* Sales_Users → Sales Share
* Operations_Users → Operations Share
* Executives → Executive Share
* IT_Admins → IT Share

---

## Group Policy Management

Configured domain-wide security policies using Group Policy.

### Password Policy

* Password Complexity Enabled
* Minimum Password Length: 8 Characters
* Password History Enforcement
* Maximum Password Age Configuration

### Account Lockout Policy

* Account Lockout Threshold: 5 Failed Attempts
* Lockout Duration: 15 Minutes
* Counter Reset: 15 Minutes

### Security Policies

* Company Security Policy GPO
* Administrative Restrictions
* User Security Controls

---

## PowerShell Automation

Developed PowerShell scripts to automate:

* Organizational Unit creation
* User provisioning
* Security group creation
* Group membership assignment
* Shared folder deployment

This reduced manual administrative effort and demonstrated Windows automation capabilities.

---

## Skills Demonstrated

* Windows Server 2022 Administration
* Active Directory Administration
* DNS Administration
* Group Policy Management
* Identity and Access Management (IAM)
* Role-Based Access Control (RBAC)
* NTFS Permissions
* Shared Folder Management
* PowerShell Automation
* User Provisioning
* Help Desk Operations
* Systems Administration

---

## Future Improvements

* DHCP Configuration
* Windows 11 Domain-Joined Client
* Drive Mapping via Group Policy
* Microsoft Intune Integration
* Microsoft Entra ID Integration
* Patch Management
* Ticketing System Integration
* Security Monitoring with Wazuh

---

## Project Outcome

Built and administered a simulated enterprise Active Directory environment containing multiple departments, security groups, shared resources, access controls, PowerShell automation, and security policies to replicate real-world IT administration workflows.
