---
title: Docker
menu: main
---
[Docker](http://www.docker.com) is the world’s leading software containerization platform.

To let Docker use another path for the images and containers:
```
$ vim /etc/default/docker
vim> DOCKER_OPTS="-g /volumes3/docker"
```

To interactively run a custom program, e.g. /bin/bash, in a running container:
```
$ docker exec -ti <container> /bin/bash
```

To obtain the host name and port number of a container:
```
$ docker inspect --format='{{(index (index .NetworkSettings.Ports "80/tcp") 0).HostPort}}' <container>
```

To link containers together:
```
$ docker run --name <container> --link <container>:<image> -P -d <image>
```

To list all running and stopped containers:
```
$ docker ps -a
```

To stop all running containers:
```
$ docker ps -q | xargs docker stop
```

To clean up all containers and images:
```
$ docker ps -q -a | xargs docker rm -v && docker images -q | xargs docker rmi -f
```

A large sheet with common Docker commands can be found [here](https://github.com/wsargent/docker-cheat-sheet).

Use [Docker Compose](http://docs.docker.com/compose/) to run multiple containers together.

[Docker Kitematic](https://kitematic.com): a GUI for Docker containers. Is [Linux support](https://github.com/kitematic/kitematic/issues/49) still pending?

[Netshare](http://netshare.containx.io/) a Docker plugin to mount network storage (NFS, AWS EFS, CIFS) in a container.

Not running (completed) containers and unused images will stay on your system until removed this will take up (quite) some disk space. To remove unused Docker images and completed containers use [Docker-GC|https://github.com/spotify/docker-gc].
```
$ docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v /etc:/etc:ro spotify/docker-gc
```
