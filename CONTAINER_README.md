# DOCKER CONTAINER

## Run the container from image
```
docker run <image-name>
docker run -p 9000:80 <image-name>:<tag> 
docker run -dp 127.0.0.1:3000:3000 <image-name>
docker run --name <container_name> <image_name>
```
* -d ==> detach mode
* -p ==> publish container, **host-port:docker-port**
* --name ==> give name of the container

## List of container
```
docker ps (or) docker container ps
docker ps -a
docker container <container-name>
```
* container-name ==> to get full details of a container

## stop container
```
docker stop <container-id>
docker stop $(docker ps -aq)
```
* docker ps -aq => To stop all containers
## start stopped container
```
docker start <container-id>
```

## Restart
```
docker restart <container-id>
```

## Inspection
```
docker inspect <container-id>
```

## Remove container
```
docker rm <container-name or container-id>
docker rm $(docker ps -aq)
```
* docker ps -aq => to remove all containers

## Execute
```
docker exec <container-id>
docker exec -it <container-id> echo "Hello World!"
```
* -it => open in the interactive mode
* echo "Hello World!" => print message inside the container

## Open ubuntu bash
```
docker run -it ubuntu bash
```
* Pull ubuntu image from remote registry
* -it ==> open in the interactive mode
