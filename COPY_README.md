# DOCKER COPY

We can copy the file from container to host and vice varsa

## Copy from the container
```
docker cp <container-id>:/<file-path-in-container> <file-path-in-host>
```
Example: **docker cp 135950565ad8:/geeksforgeeks.txt ~/Desktop/geeksforgeeks.txt**

## Copy the file from host to container
```
docker cp <file-path-in-host> <container-id>:/<file-path-in-container>
```
