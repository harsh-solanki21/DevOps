# Docker Image

### List the images

```bash
$ docker image ls
# OR
$ docker images
```

### Pull images

```bash
$ docker pull [IMAGE]
```

### Remove image

```bash
$ docker image rm [IMAGE]
```

### Remove all images

```bash
$ docker rmi $(docker images -aq)
```

<br />

## Image Tagging and Pushing to DockerHub

### Retag existing image

```bash
$ docker image tag nginx harsh21/nginx
```

### Upload to dockerhub

```bash
$ docker image push harsh21/nginx
```

### To login

```bash
$ docker login
```

### Add tag to new image

```bash
$ docker image tag harsh21/nginx harsh21/nginx:testing
```

### Build image from dockerfile

```bash
$ docker image build -t [REPO_NAME] .
```

### Tag and push to Dockerhub

```bash
$ docker image tag nginx-website:latest harsh21/nginx-website:latest

$ docker image push harsh21/nginx-website
```

<br />

### IMP: Caching & Ordering

- If you re-run the build, it will be quick because everythging is cached.
- If you change one line and re-run, that line and everything after will not be cached
- Keep things that change the most toward the bottom of the Dockerfile
