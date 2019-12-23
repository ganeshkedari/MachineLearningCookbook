# Docker

## Stop all Containers 
docker container stop $(docker container ls -aq)

## Remove all Containers 
docker container prune

## Remove all unused images
docker image prune -a

## Clean Docker Environment
docker container stop $(docker container ls -aq)
docker container prune -f
docker image prune -a -f