# Docker

## Remove all Containers 
docker container stop $(docker container ls -aq)
docker container prune


## Remove all unused images
docker image prune -a