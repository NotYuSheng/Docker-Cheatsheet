# Docker-Cheatsheet

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

Auto scroll logs
```
docker logs -f --tail <container-id>
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

List volume(s)
```
docker volume ls
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

## Common Issue(s):
### Error: 
> docker: Got permission denied while trying to connect to the Docker daemon socket at ...

### Solution:
1. Add current user to docker group
```
sudo usermod -aG docker $USER
```
2. Verify docker can be ran
```
docker ps -a
```
3. Reboot if error persist
```
sudo reboot
```
