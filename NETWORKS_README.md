# DOCKER NETWORKS

## Running sample containers
```
docker run -it --name webcon -d httpd
docker run -it --name dbcon  -e MYSQL_ROOT_PASSWORD=1234 -d mysql
```

## Network
```
docker network inspect bridge
```
to know assinged default networks to the container



## Create a network
```
docker network create <bridge_name> 
docker network create --subnet <your_subnet> --gateway <Your_gateway> bridgename
```
* --subnet ==> configure subnet
* --gateway ==> configure gateway

## List the networks
```
docker network ls
```

## Assign a network when starting the container
```
docker run --name <container_name> --net=<custom_net> -d <image_name>
```

