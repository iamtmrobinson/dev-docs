# Docker

## General Admin

Get available images:
```
docker images
```

Run an image in a container:
```
docker run {IMAGE_NAME}
```

List running containers (including their CONTAINER_ID):
```
docker ps
```

SSH into a running container:
```
docker exec -it {CONTAINER_ID} /bin/bash
```

Or if you are trying to debug something and want a container that exits immediately to keep running while you SSH in, then run:
```
docker run -it {IMAGE_NAME}
```

Kill a single container (useful for when a running container has taken control of a shell):
```
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

## Working with Applications

Expose your application via a port on localhost, e.g. if your npm application is running on `3000` and your Dockerfile `EXPOSE`s `8080` then:
```
docker run -p 8080:3000 {IMAGE_NAME}
```