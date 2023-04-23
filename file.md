### Container Cheat Sheet
docker run -d -p 8080:80 --name "webserver" nginx [Detached mode -d]
docker ps -a (list running and stopped containers)
docker start [containerName]
docker pull [ImageName]
docker container exec -it webserver bash
docker stop webserver
docker rm webserver
docker rmi nginx


docker build -t [name : tag] .
docker build -t [name : tag] -f [fileName]
docker tag [imageName] [name:tag]


#build
docker build -t webserver-image:v1 .

#run docker run -d -p 8080:80 webserver-image:v1

#display
curl localhost:8080

### Volume Cheat Sheet
docker create volume [volumeName] ## creates a new volume
docker volume ls ## Lists  the volumes


docker build -t [name : tag] .
docker volume inspect [volumeName] ## displays the volume info
docker volume rm [volumename] ## Deletes a volume
docker volume prume ## Deletes all volumes not mounted

### YAML LINT
www.yamllint.com