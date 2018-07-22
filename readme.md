# Docker Cheatsheet

## Dockerizing an app

Basic process is like this:

Create a dockerfile
Find base image with roughly the stack you want
RUN commands are used for building the image
CMD commands are executed when the image starts
docker build . -t name

## Docker Run
Single container 

```docker run -p 127.0.0.1:80:80 <container name>```

## Docker Compose

Describes set of docker images to run
By default will be on the same docker network

```docker-compose up```

docker_compose.yml file format: https://docs.docker.com/compose/compose-file/#args

## Docker Swarm

Intro: https://www.youtube.com/watch?v=KC4Ad1DS8xU

### Setting up first manager
* Run `docker swarm init` on first machine to create manager (https://docs.docker.com/engine/reference/commandline/swarm_init/)
* Run `docker swarm join <ipaddress>` on subsequent machines that are running docker to join swarm as worker (https://docs.docker.com/engine/reference/commandline/swarm_join/)

### Compose
* Run `docker stack deploy --compose-file=<docker-compose> <appname>

## Debugging

### “Unable to connect”
Container probably doesn’t have the right port(s) exposed

### “Connection reset”
Dockerized application isn’t serving externally
