# DOCKER NETWORKS

## Types of network drivers
* bridge - is default network
* host - Remove network isolation between the container and docker host
* none - Completely isolate a container from host and other containers
* overlay - Connect multiple docker deamons together
* ipvlan - 	IPvlan networks provide full control over both IPv4 and IPv6 addressing.
* macvlan - Assign a MAC address to a container.
 
## Running sample containers
```
docker run -it --name webcon -d httpd
docker run -it --name dbcon  -e MYSQL_ROOT_PASSWORD=1234 -d mysql
```

## Network Inspect
```
docker network inspect bridge
docker network inspect <network-name>
```
To get details of a network


## Create a network
```
docker network create <bridge_name> 
docker network create --subnet <your_subnet> --gateway <Your_gateway> bridgename
```
* --subnet ==> configure subnet
* --gateway ==> configure gateway

## Connect network
```
docker network connect <network-name> <container-name or id>
```
Used to connect a running container to an existng network

## Disconnect network
```
docker network disconnect <network-name> <container-name>
```
Used to remove container from the network

## List the networks
```
docker network ls
```

## Assign a network when starting the container
```
docker run --name <container_name> --net=<custom_net> -d <image_name>
```

## Remove network
```
docker network rm <name>
docker network prune
```
* prune ==> remove all unused networks
