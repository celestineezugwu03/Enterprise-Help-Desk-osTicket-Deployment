# osTicket Installation Guide

## Overview

This guide documents the installation and deployment of osTicket within a VMware Workstation homelab environment.

The deployment uses an Ubuntu Server VM to host the osTicket application and a Windows Client VM to access and test the help desk system.

---

## Environment

### Server

| Component | Technology |
|---|---|
| Virtualization | VMware Workstation |
| Operating System | Ubuntu Server 24.04 LTS |
| Web Server | Apache2 |
| Database | MariaDB |
| Application Runtime | PHP |
| Help Desk Platform | osTicket |

### Client

- Windows Client VM
- Used to access and test the osTicket web interface
- Connected to the isolated lab network

---

# Installation

## 1. Update Ubuntu

Before installing the application stack, the Ubuntu Server was updated.

```bash
sudo apt update
sudo apt upgrade -y
