# Docker Containers

### Create and run a container in foreground

```bash
$ docker container run -it -p 80:80 nginx
```

### Create and run a container in background

```bash
$ docker container run -d -p 80:80 nginx
```

### Naming Containers

```bash
$ docker container run -d -p 80:80 --name nginx-server nginx
```

### List running containers

```bash
$ docker container ls
# OR
$ docker ps
```

### List all containers (Even if not running)

```bash
$ docker container ls -a
```

### Stop container

```bash
$ docker container stop [ID]
```

### Stop all running containers

```bash
$ docker stop $(docker ps -aq)
```

### Remove container (Can not remove running containers, must stop first)

```bash
$ docker container rm [ID]
```

### To remove a running container use force (-f)

```bash
$ docker container rm -f [ID]
```

### Remove multiple containers

```bash
$ docker container rm [ID] [ID] [ID]
```

### Remove all containers

```bash
$ docker rm $(docker ps -aq)
```

### Get container logs

```bash
$ docker container logs [NAME / ID]
```

### List processes running in container

```bash
$ docker container top [NAME]
```

<br />

### Some sample container creation

```bash
# Nginx
$ docker container run -d -p 80:80 --name nginx nginx (-p 80:80 is optional as it runs on 80 by default)

# Apache
$ docker container run -d -p 8080:80 --name apache httpd

# MongoDB
$ docker container run -d -p 27017:27017 --name mongo mongo

# MySQL
$ docker container run -d -p 3306:3306 --name mysql --env MYSQL_ROOT_PASSWORD=123456 mysql
```

<br />

## Container Info

### View info on container

```bash
$ docker container inspect [NAME]
```

### Specific property (--format)

```bash
$ docker container inspect --format '{{ .NetworkSettings.IPAddress }}' [NAME]
```

### Performance stats (cpu, mem, network, disk, etc)

```bash
$ docker container stats [NAME]
```

<br />

## Accessing Containers

### Create new nginx container with bash

```bash
$ docker container run -it --name [NAME] nginx bash
```

### Run / Create Ubuntu container

```bash
$ docker container run -it --name ubuntu ubuntu
# no `bash` because ubuntu uses bash by default
```

You can also make it so when you exit the container does not stay by using the `-rm` flag

```bash
$ docker container run --rm -it --name [NAME] ubuntu
```

### Access an already created container, start with -ai

```bash
$ docker container start -ai ubuntu
```

### Use exec to edit config, etc

```bash
$ docker container exec -it mysql bash
```

### Alpine is a very small Linux distro, good for docker

```bash
$ docker container run -it alpine sh
# use `sh` beecause it does not include bash
```
