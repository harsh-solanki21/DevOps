# Docker Networking

- Docker networking allows containers to communicate with each other.

- `bridge` is the default network.

#### Drivers

- The following network drivers are available by default, and provide core networking functionality:

| Driver  | Description                                                              |
| ------- | ------------------------------------------------------------------------ |
| bridge  | The default network driver.                                              |
| host    | Remove network isolation between the container and the Docker host.      |
| none    | Completely isolate a container from the host and other containers.       |
| overlay | Overlay networks connect multiple Docker daemons together.               |
| ipvlan  | IPvlan networks provide full control over both IPv4 and IPv6 addressing. |
| macvlan | Assign a MAC address to a container.                                     |

<br />

### Get port

```bash
$ docker container port [NAME]
```

### Inspect network

```bash
$ docker network inspect [NETWORK_NAME]
```

### List networks

```bash
$ docker network ls
```

### Create network

```bash
$ docker network create [NETWORK_NAME]
```

### Remove one or more networks

```bash
$ docker network rm
```

### Remove all unused networks

```bash
$ docker network prune
```

### Create container on network

```bash
$ docker container run -d --name [NAME] --network [NETWORK_NAME] nginx
```

### Connect existing container to network

```bash
$ docker network connect [NETWORK_NAME] [CONTAINER_NAME]
```

### Disconnect container from network

```bash
$ docker network disconnect [NETWORK_NAME] [CONTAINER_NAME]
```
