## Useful Docker commands
### Basic
Works in terminal, command prompt, powershell, bash

command | description
------- | -------
`docker images` | List docker images on your machine
`docker pull IMAGE_NAME` | download an image from repository (i.e. dockerhub.com)
`docker rmi IMAGE_NAME_OR_PART_OF_HASH` | Remove a docker image
`docker run -it IMAGE_NAME ` | Run a command in a new container in an interactive tty
`docker run -d IMAGE_NAME` |  Run a command in a container
`docker ps` | List all running containers
`docker ps --all` | List all containers
`docker start CONTAINER_NAME_OR_PART_OF_HASH` | Start a stopped container
`docker stop CONTAINER_NAME_OR_PART_OF_HASH` | Stop a running container
`docker stop CONTAINER_NAME_OR_PART_OF_HASH` | Stop a docker container
`docker rm CONTAINER_NAME_OR_PART_OF_HASH` | Remove a docker container
`docker exec -it CONTAINER_NAME_OR_PART_OF_HASH /bin/sh` | Start a shell in a running container
`docker exec -it CONTAINER_NAME_OR_PART_OF_HASH /bin/bash` | Start a bash shell in a running container
`docker inspect CONTAINER_NAME_OR_PART_OF_HASH` | Information about the container
`docker network list` | List all docker networks
`docker network inspect NETWORK_NAME` | Information about the docker network

### Docker Compose 
command | description
------- | -------
`docker-compose up` | Start the containers
`docker-compose up -d` | Start the containers detached from console (i.e. a Daemon running in the background)
`docker-compose down` | Stop the containers
`docker-compose build` | Build/Rebuild the images for the containers

### Remove all dangling images
 docker rmi $(docker images -f "dangling=true" -q)