# Wanderer Docker Compose


## Docker Compose YAML
The docker compose yaml is based on the file provided in the wanderer repo:
https://raw.githubusercontent.com/open-wanderer/wanderer/main/docker-compose.yml  
Only small adjustments for convenience were made.

## Setup
To setup the needed variables, setup an environment file `.env` with the following content
```sh
# Base dir for data storage
BASE_DIR=
# Port to host app on
APP_PORT=
# Master key for search engine (at least 16 byte)
MEILI_MASTER_KEY=
# Database encryption key (at least 16 byte)
POCKETBASE_ENCRYPTION_KEY=
```
Create random byte strings with openssl, for example,
```
openssl rand -hex <length>
```

## Control Container
To start, stop, and restart the container, use
```
docker compose up|stop|restart
```