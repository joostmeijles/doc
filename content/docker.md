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

A large sheet with common Docker commands can be found [here](https://github.com/wsargent/docker-cheat-sheet).

Use [Docker Compose](http://docs.docker.com/compose/) to run multiple containers together.

[Docker Kitematic](https://kitematic.com): a GUI for Docker containers. [Linux support](https://github.com/kitematic/kitematic/issues/49) still pending? 
