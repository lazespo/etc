## Install EspoCRM with Docker

You can use Docker Compose to run EspoCRM in an isolated environment built with Docker containers. 

EspoCRM image requires to run MySQL server:

```
$ docker run --name mysql -e MYSQL_ROOT_PASSWORD=password -d mysql:8 --default-authentication-plugin=mysql_native_password
```
- `mysql` — name of container,
- `MYSQL_ROOT_PASSWORD=password` — you can change `password` to any password you want,
- `mysql:8` — image version.

## Install EspoCRM with Docker Compose

You can use Docker Compose to run EspoCRM in an isolated environment built with Docker containers. Before starting, make sure you have [Compose](https://docs.docker.com/compose/install/) installed.

1. Create an empty directory.

```
$ mkdir espocrm-docker
```

2. Change into this directory.

```
$ cd espocrm-docker/
```

3. Create a **`docker-compose.yml`** file:

```
version: '3.8'

services:

  mysql:
    image: mysql:8
    container_name: mysql
    command: --default-authentication-plugin=mysql_native_password    
    environment:
      MYSQL_ROOT_PASSWORD: root_password
      MYSQL_DATABASE: espocrm
      MYSQL_USER: espocrm
      MYSQL_PASSWORD: database_password
    volumes:
      - mysql:/var/lib/mysql
    restart: always

  espocrm:
    image: espocrm/espocrm
    container_name: espocrm
    environment:
      ESPOCRM_DATABASE_HOST: mysql
      ESPOCRM_DATABASE_USER: espocrm
      ESPOCRM_DATABASE_PASSWORD: database_password
      ESPOCRM_ADMIN_USERNAME: admin
      ESPOCRM_ADMIN_PASSWORD: password
      ESPOCRM_SITE_URL: "http://localhost:8080"
    volumes:
      - espocrm:/var/www/html
    restart: always
    ports:
      - 8080:80

  espocrm-daemon:
    image: espocrm/espocrm
    container_name: espocrm-daemon
    volumes:
      - espocrm:/var/www/html
    restart: always
    entrypoint: docker-daemon.sh

  espocrm-websocket:
    image: espocrm/espocrm
    container_name: espocrm-websocket    
    environment:
      ESPOCRM_CONFIG_USE_WEB_SOCKET: "true"
      ESPOCRM_CONFIG_WEB_SOCKET_URL: "ws://localhost:8081"
      ESPOCRM_CONFIG_WEB_SOCKET_ZERO_M_Q_SUBSCRIBER_DSN: "tcp://*:7777"
      ESPOCRM_CONFIG_WEB_SOCKET_ZERO_M_Q_SUBMISSION_DSN: "tcp://espocrm-websocket:7777"
    volumes:
      - espocrm:/var/www/html
    restart: always
    entrypoint: docker-websocket.sh
    ports:
      - 8081:8080

volumes:
  mysql:
  espocrm:
```
More about *Installation Enviroments* you can find [here](#installation-environments).

4. Build EspoCRM project from directory.

```
$ docker compose up -d
```

5. Bring up EspoCRM in a web browser. You can use http://localhost as the IP address, and open http://localhost:80 in a web browser.

### Enter the EspoCRM container

In order to enter the container and view the files, make a rebuild, etc., use the following command (`espocrm` is your container name):

```
$ docker exec -it espocrm bash
```

### Shutdown and cleanup

The `docker compose down` command removes the containers and default network, but preserves EspoCRM database.

The `docker compose down --volumes` removes the containers, default network, and the EspoCRM database.

### Installation Environments

This is one-time environment variables which are using only for the fresh installation. If you need to define configuration options on the container startup, see the Config Environments.

- `ESPOCRM_DATABASE_HOST`

MySQL host name for EspoCRM. The default value is `mysql`.

- `ESPOCRM_DATABASE_NAME`

Database name for EspoCRM. The default value is `espocrm`.

- `ESPOCRM_DATABASE_USER`

Database user for EspoCRM. The default value is `root`.

- `ESPOCRM_DATABASE_PASSWORD`

Database password for EspoCRM. The default value is `password`.

- `ESPOCRM_ADMIN_USERNAME`

User name for an administrator of EspoCRM. The default value is `admin`.

- `ESPOCRM_ADMIN_PASSWORD`

User password for an administrator of EspoCRM. The default value is `password`.

- `ESPOCRM_SITE_URL`

The URL of EspoCRM. This option is very important for normal operating of EspoCRM. Examples: `http://172.20.0.100:8080`, `http://my-crm.local`.
