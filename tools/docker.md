# Docker

Get available images:
```
docker images
```

Run an image in a container:
```
docker run {IMAGE_NAME}
```

Kill a single container (useful for when a running container has taken control of a shell):
```
docker ps
docker kill {CONTAINER_ID}
```

Stop all running containers:
```
docker stop $(docker ps -aq)
```

Remove all containers:
```
docker rm $(docker ps -aq)
```

Clean:
```
docker-sync clean
```
