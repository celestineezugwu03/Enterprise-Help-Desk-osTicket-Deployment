# Project Overview

## Project Title

Enterprise Help Desk - osTicket Deployment Lab

## Overview

This project focuses on deploying an enterprise-style IT help desk using osTicket within a VMware Workstation homelab.

The project builds upon my previous Active Directory Enterprise Lab, where I established a Windows-based infrastructure using Windows Server, Active Directory Domain Services, DNS, Group Policy, organizational units, user accounts, and file permissions.

For this project, I expanded the environment by introducing an Ubuntu Server responsible for hosting osTicket. The server uses Apache as the web server, PHP as the application runtime, and MariaDB as the database backend.

The goal is to demonstrate how different systems can work together to provide an internal IT support service.

## Problem

A simulated organization needs a centralized method for employees to submit and track IT support requests.

Instead of relying on informal communication methods, such as direct messages or email, the organization can use a centralized ticketing platform to document incidents, assign responsibility, track progress, and record resolutions.

## Solution

I deployed osTicket on an Ubuntu Server within my existing VMware homelab.

The Ubuntu server provides:

- Apache web server
- PHP application environment
- MariaDB database
- osTicket help desk application

Windows client systems access the help desk through the lab network.

## Project Architecture

The general architecture is:

Windows Client
        |
        | Host-Only Network
        |
Ubuntu Server
        |
   Apache + PHP
        |
     osTicket
        |
     MariaDB

The Ubuntu server also maintains NAT connectivity for Internet access and software updates.

## Objectives

- Deploy Ubuntu Server in VMware Workstation.
- Configure Apache2.
- Install and configure MariaDB.
- Install PHP and required dependencies.
- Deploy osTicket.
- Configure Linux file permissions.
- Configure VMware virtual networking.
- Establish communication between Windows clients and the Ubuntu server.
- Configure the osTicket database.
- Validate the ticketing platform.
- Document troubleshooting and configuration decisions.

## Current Status

The osTicket application has been successfully installed.

The Windows client is able to communicate with the Ubuntu server through the lab network using the Ubuntu Host-Only address:

`192.168.56.110`

The PHP IMAP extension has not been configured because email-to-ticket functionality is not currently required for the initial implementation.

## Project Relationship

This project is an extension of my Active Directory Enterprise Lab.

The Active Directory project established the Windows infrastructure and simulated organizational services.

This project adds an IT service management platform to that infrastructure.

Together, the projects demonstrate progression from building infrastructure to deploying services that support end users.

## Skills Demonstrated

- Linux Server Administration
- Windows Server Administration
- VMware Workstation
- Virtual Networking
- Apache
- PHP
- MariaDB
- osTicket
- Database Administration
- File Permissions
- Troubleshooting
- IT Service Management
- Technical Documentation

## Future Improvements

Potential future improvements include:

- Active Directory/LDAP authentication
- Email-to-ticket integration
- HTTPS/SSL
- Automated backups
- Monitoring
- Centralized logging
- Additional ticket workflows
