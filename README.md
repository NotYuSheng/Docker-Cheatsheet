# Docker-cheatsheet

## Docker
List Docker container(s)
```
docker ps -a
```

Check container(s) log(s)
```
docker-compose logs
```

Check container build status
```
docker logs <container-id>
```

Get interactive shell after container has started
```
docker exec -it <container-id> /bin/bash
```

Start docker container after host restart
```
docker container start <container-id>
```

Delete all container(s) including its volume(s) use
```
docker rm -vf $(docker ps -aq)
```

Delete all image(s)
```
docker rmi -f $(docker images -aq)
```

## Docker-compose
Build the Docker image(s):
```
docker-compose build
```

Run image(s)
```
docker-compose up -d
```
