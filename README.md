# Docker Olog Deployment Files

Deployment files for the Olog docker containers.

## Environment variables

For a description of the environment variables needed for this project, consult this [link](https://github.com/lnls-sirius/docker-olog-server).

## Deployment with Docker Compose

### Executing `docker-compose.yml`

Clone and change your working directory to the project folder. Then, execute `docker-compose up -d` to deploy all containers and `docker-compose down` to stop them. Remember to update the volume bindings with paths in your system!

### Setting `systemd` services up

Execute `make install` with `root` rights in order to copy all required files and start systemd service.

## Deployment with Docker Swarm

Enter `swarm/` directory and execute `docker stack deploy -c docker-swarm olg-con` to deploy the services into the swarm and `docker stack rm olog-con` to shut them down.
