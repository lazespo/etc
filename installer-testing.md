# Manual Testing Map

## Install.sh

Production: `wget https://github.com/espocrm/espocrm-installer/releases/latest/download/install.sh`

Master: `wget -N https://raw.githubusercontent.com/espocrm/espocrm-installer/master/install.sh`

-----------

## Options testing

#### `-y` or `--yes`

Skip confirmation prompts during installation.

- [x] SUCCESS
- [ ] FAILED

```
bash install.sh -y
```

Terminal result:

```
Waiting for the first-time EspoCRM configuration.
This may take up to 5 minutes.
...

The installation has been successfully completed.

IMPORTANT: Your EspoCRM instance is working in HTTP mode.
If you want to install with SSL/TLS certificate, use "--ssl" option. For more details, please visit https://docs.espocrm.com/administration/installation-by-script#installation-with-ssltls-certificate.

Login data/information to your EspoCRM instance:
URL: http://192.168.0.8
Username: admin
Password: 68ad301ed5fc

Your instance files are located at: "/var/www/espocrm".
```

#### `--domain`

Define your domain. Ex. `--domain=my-domain.com` (use in installation mode with SSL/TLS or Let's Encrypt certificate).

- [x] SUCCESS
- [ ] FAILED

```
bash install.sh --domain
```

Terminal result:

```
This script will install EspoCRM with all the needed prerequisites (including Docker, Docker-compose, Nginx, PHP, MySQL).
Do you want to continue the installation? [y/n] y
NOTICE: For using your own SSL/TLS certificates you have to setup them manually after the installation.

Summary information:
  Domain: espo.local
  Mode: Own SSL/TLS certificate
Do you want to continue? [y/n] y
Waiting for the first-time EspoCRM configuration.
This may take up to 5 minutes.
...

The installation has been successfully completed.

IMPORTANT: Your EspoCRM instance is working in insecure mode with a self-signed certificate.
You have to setup your own SSL/TLS certificates. For more details, please visit https://docs.espocrm.com/administration/installation-by-script#2-own-ssltls-certificate.

Login data/information to your EspoCRM instance:
URL: https://espo.local
Username: admin
Password: ebf29e475135
```

#### `--email`

Email address for Let's Encrypt certificate. Ex. `--email=email@my-domain.com`.

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --email
```

Terminal result:

```
```

#### `--clean`

Clean the existing EspoCRM installation and start a new one. This option can be used if you have already installed EspoCRM. Ex. `--clean`.

- [x] SUCCESS
- [ ] FAILED

```
bash install.sh --clean
```

Terminal result:

```
This script will install EspoCRM with all the needed prerequisites (including Docker, Docker-compose, Nginx, PHP, MySQL).
Do you want to continue the installation? [y/n] y
Cleaning the previous installation...
Creating a backup...
Backup is created: /home/renata/espocrm-backup/2022-12-05_124638

Summary information:
  Domain: 192.168.0.8
  Mode: HTTP only
Do you want to continue? [y/n] y  
Waiting for the first-time EspoCRM configuration.
This may take up to 5 minutes.
...

The installation has been successfully completed.

IMPORTANT: Your EspoCRM instance is working in HTTP mode.
If you want to install with SSL/TLS certificate, use "--ssl" option. For more details, please visit https://docs.espocrm.com/administration/installation-by-script#installation-with-ssltls-certificate.

Login data/information to your EspoCRM instance:
URL: http://192.168.0.8
Username: admin
Password: ee00fc212086

Your instance files are located at: "/var/www/espocrm".
```

#### `--mysqlRootPassword`

Define your own MySQL root password instead of the automatically generated one. Ex. `--mysqlRootPassword=my-password`.

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --mysqlRootPassword
```

Terminal result:

```
```

- [ ] Check password via CLI in docker container (`espocrm-mysql`) or in the phpMyAdmin.

`sudo docker exec --user "www-data" -it espocrm-mysql /bin/bash`

#### `--mysqlPassword`

Define your own MySQL password for EspoCRM installation. Ex. `--mysqlPassword=my-password`.

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --mysqlPassword=my-password
```

Terminal result:

```
```

- [ ] Check password via CLI in docker container (`espocrm-mysql`) or in the phpMyAdmin.

`sudo docker exec --user "www-data" -it espocrm-mysql /bin/bash`

#### `--adminUsername`

Define a username of your EspoCRM administrator. Ex. `--adminUsername=admin`.

- [x] SUCCESS
- [ ] FAILED

```
bash install.sh --adminUsername=admin
```

Terminal result:

```
This script will install EspoCRM with all the needed prerequisites (including Docker, Docker-compose, Nginx, PHP, MySQL).
Do you want to continue the installation? [y/n] y
Cleaning the previous installation...
Creating a backup...
Backup is created: /home/renata/espocrm-backup/2022-12-05_125156

Summary information:
  Domain: 192.168.0.8
  Mode: HTTP only
Do you want to continue? [y/n] y
Waiting for the first-time EspoCRM configuration.
This may take up to 5 minutes.
...

The installation has been successfully completed.

IMPORTANT: Your EspoCRM instance is working in HTTP mode.
If you want to install with SSL/TLS certificate, use "--ssl" option. For more details, please visit https://docs.espocrm.com/administration/installation-by-script#installation-with-ssltls-certificate.

Login data/information to your EspoCRM instance:
URL: http://192.168.0.8
Username: renata
Password: 0b6baf06280d

Your instance files are located at: "/var/www/espocrm".
```

- [x] Check username in instance.

#### `--adminPassword`

Define a password of EspoCRM administrator. Ex. `--adminPassword=admin-password`.

- [x] SUCCESS
- [ ] FAILED

```
bash install.sh --adminPassword=admin-password
```

Terminal result:

```
This script will install EspoCRM with all the needed prerequisites (including Docker, Docker-compose, Nginx, PHP, MySQL).
Do you want to continue the installation? [y/n] y
Cleaning the previous installation...
Creating a backup...
Backup is created: /home/renata/espocrm-backup/2022-12-05_124846

Summary information:
  Domain: 192.168.0.8
  Mode: HTTP only
Do you want to continue? [y/n] y
Waiting for the first-time EspoCRM configuration.
This may take up to 5 minutes.
...

The installation has been successfully completed.

IMPORTANT: Your EspoCRM instance is working in HTTP mode.
If you want to install with SSL/TLS certificate, use "--ssl" option. For more details, please visit https://docs.espocrm.com/administration/installation-by-script#installation-with-ssltls-certificate.

Login data/information to your EspoCRM instance:
URL: http://192.168.0.8
Username: admin
Password: 1

Your instance files are located at: "/var/www/espocrm".
```

- [x] Check password in instance.

#### `--command`

Update the command.sh for the existing instllation. Ex. `--command`.

- [x] SUCCESS
- [ ] FAILED

```
bash install.sh --command
```

Terminal result:

```
Done
```

#### `--backupPath`

A path for the backup. Ex. `--backupPath="/backup"`.

- [ ] SUCCESS
- [x] FAILED

```
bash install.sh --backupPath="/backup"
```

Terminal result:

```
This script will install EspoCRM with all the needed prerequisites (including Docker, Docker-compose, Nginx, PHP, MySQL).
Do you want to continue the installation? [y/n] y
Cleaning the previous installation...
Backup is created: /home/renata/espocrm-backup/2022-12-05_125608
```

- [ ] Check if backup directory was created in path.

-----------

## HTTP mode

#### First time installation

- [x] SUCCESS
- [ ] FAILED

```
bash install.sh
```

1. Terminal result:

```
Waiting for the first-time EspoCRM configuration.
This may take up to 5 minutes.
...

The installation has been successfully completed.

IMPORTANT: Your EspoCRM instance is working in HTTP mode.
If you want to install with SSL/TLS certificate, use "--ssl" option. For more details, please visit https://docs.espocrm.com/administration/installation-by-script#installation-with-ssltls-certificate.

Login data/information to your EspoCRM instance:
URL: http://192.168.0.8
Username: admin
Password: a58cdedeb34e

Your instance files are located at: "/var/www/espocrm".
```

2. Tested EspoCRM functionality:

- [x] Admin login
- [x] Creating a record
- [x] Adding an attachment
- [x] Check Scheduled Jobs
- [x] Check websocket

#### Reinstallation (when already installed)

- [ ] SUCCESS
- [x] FAILED

```
bash install.sh
```

2. Terminal result:

```
This script will install EspoCRM with all the needed prerequisites (including Docker, Docker-compose, Nginx, PHP, MySQL).
Do you want to continue the installation? [y/n] y

The installed EspoCRM instance is found.

Summary information:
  Domain: 192.168.0.8
  Mode: HTTP only
Do you want to continue? [y/n] y

Starting the reinstallation process...
Creating a backup...
Backup is created: /home/renata/espocrm-backup/2022-12-05_130328

Waiting for the first-time EspoCRM configuration.
This may take up to 5 minutes.

The installation has been successfully completed.

IMPORTANT: Your EspoCRM instance is working in HTTP mode.
If you want to install with SSL/TLS certificate, use "--ssl" option. For more details, please visit https://docs.espocrm.com/administration/installation-by-script#installation-with-ssltls-certificate.

Login data/information to your EspoCRM instance:
URL: http://192.168.0.8
Username: admin
Password: a58cdedeb34e

Your instance files are located at: "/var/www/espocrm".
```

3. Tested EspoCRM functionality:

- [x] Admin login
- [x] Admin password is the same as first time?
- [x] Creating a record
- [x] Adding an attachment
- [x] Check Scheduled Jobs
- [x] Check websocket

## SSL mode

### Own Certificate mode

#### First time installation

- [x] SUCCESS
- [ ] FAILED

```
bash install.sh --ssl --owncertificate
```

1. Terminal result:

```
This script will install EspoCRM with all the needed prerequisites (including Docker, Docker-compose, Nginx, PHP, MySQL).
Do you want to continue the installation? [y/n] y

NOTICE: For using your own SSL/TLS certificates you have to setup them manually after the installation.

Enter a domain name for the future EspoCRM instance (e.g. espoexample.com): espo.local

Summary information:
  Domain: espo.local
  Mode: Own SSL/TLS certificate
Do you want to continue? [y/n] y

Waiting for the first-time EspoCRM configuration.
This may take up to 5 minutes.
...

The installation has been successfully completed.

IMPORTANT: Your EspoCRM instance is working in insecure mode with a self-signed certificate.
You have to setup your own SSL/TLS certificates. For more details, please visit https://docs.espocrm.com/administration/installation-by-script#2-own-ssltls-certificate.

Login data/information to your EspoCRM instance:
URL: https://espo.local
Username: admin
Password: ebf29e475135
```

2. Tested EspoCRM functionality:

- [x] Admin login
- [x] Creating a record
- [x] Adding an attachment
- [x] Check Scheduled Jobs
- [x] Check websocket

#### Reinstallation (when already installed)

- [x] SUCCESS
- [ ] FAILED

```
bash install.sh
```

2. Terminal result:

```
This script will install EspoCRM with all the needed prerequisites (including Docker, Docker-compose, Nginx, PHP, MySQL).
Do you want to continue the installation? [y/n] y

The installed EspoCRM instance is found.
NOTICE: For using your own SSL/TLS certificates you have to setup them manually after the installation.

Enter a domain name for the future EspoCRM instance (e.g. espoexample.com): espo.local

Summary information:
  Domain: espo.local
  Mode: Own SSL/TLS certificate
Do you want to continue? [y/n] y

Starting the reinstallation process...
Creating a backup...
Backup is created: /home/renata/espocrm-backup/2022-12-05_131826

Waiting for the first-time EspoCRM configuration.
This may take up to 5 minutes.


The installation has been successfully completed.

IMPORTANT: Your EspoCRM instance is working in insecure mode with a self-signed certificate.
You have to setup your own SSL/TLS certificates. For more details, please visit https://docs.espocrm.com/administration/installation-by-script#2-own-ssltls-certificate.

Login data/information to your EspoCRM instance:
URL: https://espo.local
Username: admin
Password: ebf29e475135

Your instance files are located at: "/var/www/espocrm".
```

3. Tested EspoCRM functionality:

- [x] Admin login
- [x] Admin password is the same as first time?
- [x] Creating a record
- [x] Adding an attachment
- [x] Check Scheduled Jobs
- [x] Check websocket

### Let's Encrypt mode

#### First time installation

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --ssl --letsencrypt
```

1. Terminal result:

```
```

2. Tested EspoCRM functionality:

- [ ] Admin login
- [ ] Creating a record
- [ ] Adding an attachment
- [ ] Check Scheduled Jobs
- [ ] Check websocket

#### Reinstallation (when already installed)

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh
```

2. Terminal result:

```
```

3. Tested EspoCRM functionality:

- [ ] Admin login
- [ ] Admin password is the same as first time?
- [ ] Creating a record
- [ ] Adding an attachment
- [ ] Check Scheduled Jobs
- [ ] Check websocket

-----------
## Command.sh

### Status of services

- [ ] SUCCESS
- [ ] FAILED

```
/var/www/espocrm/command.sh status
```

Terminal result:

```
```

### Restart services

- [ ] SUCCESS
- [ ] FAILED

```
/var/www/espocrm/command.sh restart
```

Terminal result:

```
```

### Start services

- [ ] SUCCESS
- [ ] FAILED

```
/var/www/espocrm/command.sh start
```

Terminal result:

```
```

### Build and start services

- [ ] SUCCESS
- [ ] FAILED

In order to apply changes in `docker-compose.yml`.

```
/var/www/espocrm/command.sh build
```

Terminal result:

```
```

### Stop services

- [ ] SUCCESS
- [ ] FAILED

```
/var/www/espocrm/command.sh stop
```

Terminal result:

```
```

### EspoCRM rebuild

- [ ] SUCCESS
- [ ] FAILED

```
/var/www/espocrm/command.sh rebuild
```

Terminal result:

```
```

### EspoCRM upgrade

- [ ] SUCCESS
- [ ] FAILED

```
/var/www/espocrm/command.sh upgrade
```

Terminal result:

```
```

### EspoCRM logs

- [ ] SUCCESS
- [ ] FAILED

```
/var/www/espocrm/command.sh logs
```

Terminal result:

```
```

### Backup

- [ ] SUCCESS
- [ ] FAILED

Create a full backup of EspoCRM.

```
/var/www/espocrm/command.sh backup "BACKUP_DIRECTORY"
```

An example: `/var/www/espocrm/command.sh backup /var/www/espocrm-backup`.

Terminal result:

```
```

- [ ] Check if backup was recreated in path.

### Restore

- [ ] SUCCESS
- [ ] FAILED

Restore the backup created by the `backup` command.

```
/var/www/espocrm/command.sh restore "BACKUP_PATH"
```

An example: `/var/www/espocrm/command.sh restore "/var/www/espocrm-backup/2023-01-01_142051.tar.gz"`.

Terminal result:

```
```

- [ ] Check if data was recreated.

### Clean

- [ ] SUCCESS
- [ ] FAILED

Delete old and unnecessary files.

```
/var/www/espocrm/command.sh clean
```

Terminal result:

```
```

### Import the SQL dump

- [ ] SUCCESS
- [ ] FAILED

Import the database by the SQL dump created by `mysqldump`, `phpMyAdmin`, etc.

```
/var/www/espocrm/command.sh import-db "PATH/DB.sql"
```

An example: `/var/www/espocrm/command.sh restore "/var/www/espocrm-backup/db.sql"`.

Terminal result:

```
```

- [ ] Check if data was recreated.

### Help

- [ ] SUCCESS
- [ ] FAILED

In order to display a list of available commands.

```
/var/www/espocrm/command.sh help
```

Terminal result:

```
```

-----------

## Changing installed mode

All the actions can be applied to **already installed** EspoCRM instance.

### From HTTP to Own SSL/TLS certificate

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --ssl --owncertificate --domain=my-espocrm.com
```

Terminal result:

```
```

### From HTTP to Let's Encrypt certificate

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --ssl --letsencrypt --domain=my-espocrm.com --email=email@my-domain.com
```

Terminal result:

```
```

### From Own SSL/TLS certificate to Let's Encrypt certificate

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --ssl --letsencrypt --domain=my-espocrm.com --email=email@my-domain.com
```

Terminal result:

```
```
