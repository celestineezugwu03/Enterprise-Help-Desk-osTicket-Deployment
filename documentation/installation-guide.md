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
2. Install Apache

Apache was installed to provide the web server responsible for hosting osTicket.

sudo apt install apache2 -y

The Apache service was verified using:

sudo systemctl status apache2
3. Install MariaDB

MariaDB was installed as the database server for osTicket.

sudo apt install mariadb-server -y

The MariaDB installation was secured using:

sudo mysql_secure_installation
4. Install PHP

PHP was installed along with the modules required by osTicket.

Example modules included:

php-mysql
php-gd
php-curl
php-xml
php-mbstring
php-intl
php-zip
libapache2-mod-php
5. Download osTicket

The osTicket release was downloaded and extracted on the Ubuntu server.

The application files were then placed under:

/var/www/html/osticket
6. Configure Permissions

The web application files were assigned to the Apache web server account.

sudo chown -R www-data:www-data /var/www/html/osticket

Appropriate permissions were then applied.

7. Create the osTicket Configuration File

The osTicket installer required a writable configuration file.

The sample configuration was copied:

sudo cp /var/www/html/osticket/include/ost-sampleconfig.php \
/var/www/html/osticket/include/ost-config.php

The configuration file was temporarily made writable so the web installer could save the application configuration.

8. Configure VMware Networking

The Ubuntu VM was configured with network connectivity for both Internet access and communication with the isolated lab.

The Ubuntu server received the following Host-Only address:

192.168.56.110

This allowed the Windows Client VM to access osTicket.

9. Create the osTicket Database

A dedicated MariaDB database was created for osTicket.

CREATE DATABASE osticket;

A dedicated database user was created:

CREATE USER 'osticketuser'@'localhost'
IDENTIFIED BY 'YOUR_PASSWORD';

Permissions were granted:

GRANT ALL PRIVILEGES ON osticket.* 
TO 'osticketuser'@'localhost';

Privileges were then reloaded:

FLUSH PRIVILEGES;
10. Complete Web Installation

The osTicket installer was accessed from the Windows Client using:

http://192.168.56.110/osticket

The database settings were configured using:

Host: localhost
Database: osticket
Username: osticketuser
Password: The password created during database setup

The osTicket installation completed successfully.

11. Post-Installation Security

After confirming the installation, the configuration file should be returned to a non-writable state:

sudo chmod 644 /var/www/html/osticket/include/ost-config.php

The setup directory should also be removed:

sudo rm -rf /var/www/html/osticket/setup
Result

The Ubuntu server successfully hosts osTicket and can be accessed by the Windows Client VM over the lab network.
