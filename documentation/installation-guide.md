# Installation Guide

## Environment

The osTicket deployment was completed within VMware Workstation.

### Server

- Operating System: Ubuntu Server 24.04 LTS
- Web Server: Apache2
- Database: MariaDB
- Application Runtime: PHP
- Help Desk: osTicket

### Client

- Windows Client VM
- Used to access and test the osTicket web interface

## 1. Update Ubuntu

The Ubuntu server was updated before installing the application stack.

```bash
sudo apt update
sudo apt upgrade -y
