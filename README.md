# Enterprise-Help-Desk-osTicket-Deployment
# Enterprise Help Desk - osTicket Deployment Lab

## Overview

This project demonstrates the deployment and configuration of an
enterprise-style IT help desk using osTicket, Ubuntu Server,
Apache, PHP, and MariaDB within a VMware Workstation homelab.

The project builds upon my existing Active Directory Enterprise Lab
by introducing a Linux-based IT service management platform that can
be accessed by Windows client systems across the lab network.

## Project Architecture

Windows Client
       |
       | Host-Only Network
       |
Ubuntu Server
       |
   Apache/PHP
       |
   osTicket
       |
    MariaDB

## Environment

| Component | Technology |
|---|---|
| Hypervisor | VMware Workstation |
| Help Desk Server | Ubuntu Server 24.04 LTS |
| Web Server | Apache2 |
| Application | osTicket |
| Database | MariaDB |
| Runtime | PHP |
| Client | Windows |
| Network | VMware NAT + Host-Only |

## Objectives

- Deploy Ubuntu Server
- Configure Apache
- Configure MariaDB
- Configure PHP
- Deploy osTicket
- Configure virtual networking
- Connect Windows clients to the help desk
- Test the ticket lifecycle
- Document troubleshooting and administration

## Implementation

### 1. Ubuntu Server

Deployed Ubuntu Server as the application server within VMware.

### 2. Web Server

Installed and configured Apache2 to host the osTicket web application.

### 3. Database

Installed MariaDB and created a dedicated database and user for osTicket.

### 4. PHP

Installed PHP and required application dependencies.

### 5. osTicket

Downloaded and deployed osTicket under:

`/var/www/html/osticket`

### 6. Networking

Configured Ubuntu with:

- NAT connectivity for Internet access
- Host-Only connectivity for communication with the lab

Ubuntu lab address:

`192.168.56.110`

## Troubleshooting

Documented issues included:

- PHP IMAP dependency warning
- VMware network connectivity
- osTicket configuration file permissions
- MariaDB authentication/database credentials

Each issue was diagnosed and resolved or intentionally deferred based
on project requirements.

## Testing

The final environment will be validated by:

- Accessing osTicket from the Windows Client
- Creating a support ticket
- Assigning a ticket
- Updating ticket status
- Resolving a ticket
- Closing the ticket

## Skills Demonstrated

- Linux Administration
- Windows/Linux Integration
- VMware Virtualization
- Apache
- PHP
- MariaDB
- Virtual Networking
- Web Application Deployment
- Troubleshooting
- IT Service Management
- Technical Documentation

## Relationship to Previous Project

This project expands upon my Active Directory Enterprise Lab.

The Active Directory project established the Windows infrastructure,
while this project adds an IT service management platform running on
Linux.

Together, the projects demonstrate how different technologies can
work together within a simulated enterprise environment.

## Future Improvements

- Email-to-ticket integration
- Active Directory/LDAP authentication
- HTTPS/SSL
- Automated backups
- Monitoring
- Centralized logging
- Additional help desk workflows



Project Relationship: This project builds upon my Active Directory Enterprise Lab by adding a Linux-based IT service management platform to the existing virtualized environment. Windows client systems communicate with the Ubuntu Server hosting osTicket, creating a simulated enterprise help desk environment.
