# Docker-compose
####
### Docker compose overview 

- Compose is a tool for defining and running multi-container Docker applications. 
- Using a YAML file "docker-compose.yaml" by default, you can configure your application's as services.
- A single command can create and start all the services in one go.
- Compose works in all environments: production, staging, development, testing, as well as with CI integration.

#### Three-steps of compose process
1. Define your app’s environment with a Dockerfile so it can be reproduced anywhere.

2. Define the services that make up your app in docker-compose.yml so they can be run together in an isolated environment.

3. Finally, run docker-compose up -d and an entire applications inside containers will start.

#### Steps to install compose on Linux 
```
1. $ sudo curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
2. $ sudo chmod +x /usr/local/bin/docker-compose
3. $ docker-compose --version
```
### Features of compose 

- Using Project name you can create multiple isolated environments Dev, test , UAT , Live ... on a single host. 
- Preserve volume data when containers are created
- Only recreate containers that have changed
- Variables and moving a composition between environments

### Compose prominent commands 
- docker-compose build
- docker-compose up/down 
- docker-compose logs
- docker-compose events
- docker-compose pause/unpause
- docker-compose scale web=2 worker=3
- docker-compose start/stop/ps/rm

### STACK

A stack is a group of interrelated services that share dependencies, and can be orchestrated and scaled together. 

## Deploy stack
```
$ docker stack deploy -c docker-compose.yml webtier
$ docker stack ps webtier
$ docker service ls
```
