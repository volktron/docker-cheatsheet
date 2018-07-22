## Angular Container Setup

### Build
* First thing to do is build your angular app
* `ng build --watch` generates a `dist` folder

### Docker Container
In this cheatsheet version we use nginx:alpine as a base for our container. It will run nginx as a server to host static content, which in this case is the angular app.

#### Instructions
* Build your angular app using `ng build --watch`
* Copy `nginx.conf` to your angular app
* Copy `dockerfile` to your angular app
* Run `docker build . -t <name>` to build the container
