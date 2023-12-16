# DOCKER VOLUMES

## Remove dandling volumes
```
docker volume ls -f dangling=true
```

## Remove volume
```
docker volume rm
```

## List the volumes
```
docker volume ls
```

## Removing volume when removing container
```
docker rm -f -v <container-id>
```

## Create a volume
```
docker volume create <name>
```

## Inspect a volume
```
docker volume inspect <name>
```

## Mounting docker volumes
```
docker run -it -v <volume-name>:/<directory> --name <container-name> <image-name>
```

