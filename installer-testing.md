# Manual Testing Map

## Install.sh

Production: `wget https://github.com/espocrm/espocrm-installer/releases/latest/download/install.sh`

Master: `wget -N https://raw.githubusercontent.com/espocrm/espocrm-installer/master/install.sh`

-----------

## Options testing

#### `-y` or `--yes`

Skip confirmation prompts during installation.

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh -y
```

Terminal result:

```
```

#### `--domain`

Define your domain. Ex. `--domain=my-domain.com` (use in installation mode with SSL/TLS or Let's Encrypt certificate).

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --domain
```

Terminal result:

```
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

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --clean
```

Terminal result:

```
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

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --adminUsername=admin
```

Terminal result:

```
```

- [ ] Check username in instance.

#### `--adminPassword`

Define a password of EspoCRM administrator. Ex. `--adminPassword=admin-password`.

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --adminPassword=admin-password
```

Terminal result:

```
```

- [ ] Check password in instance.

#### `--command`

Update the command.sh for the existing instllation. Ex. `--command`.

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --command
```

Terminal result:

```
```

#### `--backupPath`

A path for the backup. Ex. `--backupPath="/backup"`.

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --backupPath="/backup"
```

Terminal result:

```
```

- [ ] Check if backup directory was created in path.

-----------

## HTTP mode

#### First time installation

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh
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

## SSL mode

### Own Certificate mode

#### First time installation

- [ ] SUCCESS
- [ ] FAILED

```
bash install.sh --ssl --owncertificate
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
