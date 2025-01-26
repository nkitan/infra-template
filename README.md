# Infrasturcture Template

This repository contains Infrastructure-as-Code for various services including the following
- postgresql cluster with pgpool and pgadmin
- keycloak server with its own postgres instance


## Requirements

- [Docker](https://www.docker.com/) / [Podman](https://podman.io/)
- [Docker-Compose](https://docs.docker.com/compose/) / [Podman-Compose](https://docs.podman.io/en/v5.1.1/markdown/podman-compose.1.html)

## Installation

1. Clone this repository

   ```sh
   git clone git@github.com:nkitan/infra-template.git
   cd infra-template
   ```
## Usage

1. Head into the directory

   ```sh
   cd <service>-cluster
   ```
2. Edit .env file for the infra you want to run and set required credentials, IPs etc

   ```sh
   vim .env
   ```
3. Run docker-compose
   ```sh
   docker-compose -f <service>-compose.yml up -d
   ```

Your infrasturcture should now be up

### Additional Commands

- `docker ps` - See running services
- `docker inspect` - inspect running services -> [docker-inspect](https://docs.docker.com/reference/cli/docker/inspect/)
- `docker exec` - run custom commands on running services -> [docker-exec](https://docs.docker.com/reference/cli/docker/container/exec/)

A complete list of docker and docker-compose commands can be found [here](https://docs.docker.com/reference/cli/docker/) and [here](https://docs.docker.com/reference/cli/docker/compose/)

## License

![AGPL3](https://img.shields.io/badge/license-AGPL-blue.svg)

[LICENSE](LICENSE) © [nkitan](https://github.com/nkitan).