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

## Docker Swarm

_TODO_

## Debugging

### “Unable to connect”
Container probably doesn’t have the right port(s) exposed

### “Connection reset”
Dockerized application isn’t serving externally
