# learn-docker

Refering this tutorial
https://www.geeksforgeeks.org/introduction-to-docker/

For express js application
https://www.geeksforgeeks.org/docker-docker-container-for-node-js/?ref=lbp

For mongo-db https://www.geeksforgeeks.org/how-to-run-mongodb-as-a-docker-container/?ref=lbp

For nginx https://www.geeksforgeeks.org/docker-container-for-nginx/?ref=lbp

For backend and frontend https://www.geeksforgeeks.org/docker-compose/?ref=lbp

## docker login
```
docker login
```
Login with docker hub credential

## docker build images

```
docker build -t <image-name>:<tag> .
docker build -t <name>:<tag>
```
* if tag is not specified, it marked as latest
* -t ==> tag name, to give name of the image
* python-test ==> name of the image
* . ==> location where the Dockerfile is present

## docker image
```
docker images (or) docker image ps
docker images <image-name>:<tag-name>
docker image prune
docker rmi -f <image-id>
docker rmi $(docker images -q)
```
* prune ==> Dangling images
* rmi -f ==> remove all versions of image
* docker images -q ==> to delete all images
## Docker tag
```
docker tag <image-name> <username>/<new-image-name>
```
* image-name ==> local image name
* username ==> remote username of public registry
* new-image-name ==> image name for public registry

## docker push
```
docker push <username>/<new-image-name>
```
Push local tagged image to remote registry

## docker pull
```
docker pull <username>/<new-image-name>
docker run <username>/<new-image-name>
docker pull <image-name>:<tag-name>
```
* pull ==> Pull the docker image from remote registry
* run ==> Pull and run the docker image from remote registry if local 
image is not present
