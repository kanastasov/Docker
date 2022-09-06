Docker commands


docker pull redis

docker images

docker run redis => start the image in the container

docker ps - showing the running containers

docker run -d redis - get the id of the container

docker stop 61b99413e3525c11f6d61c2eb9ddf7e47ebc9c08f176479312bb7cb2f187fd98 id of the docker container to stop it

docker start 61b99413e3525c11f6d61c2eb9ddf7e47ebc9c08f176479312bb7cb2f187fd98

docker ps -a  => shows running and stopped containers

docker run redis:4.0 => pulls image and starts container

docker run -p6000:6379 redis => bind the port of 6379 to 6000

docker run -p6001:6379 -d redis:4.0


docker pull => pull the image from repo local

docker run combines docker pull and docker start

docker start/stop restart container

docker run -d  => run the container detached mode => -p6000:6379 bind the port of the host to the container

docker ps -a all the containers

docker images => all the images locally


Docker commands for troubleshootin

docker logs 551adaea66d6(cotainer id)

docker logs objective_margulis(cotainer name)

docker run -d -p6001:6379 --name redis-older redis:4.0

docker run -d -P --name redis-older redis:4.0

docker run -d -P --name redis-latest redis

docker logs redis-older


docker exec -it 40d26f4e1b07(container id) /bin/bash

ls / pwd 

cd /

ls

env


------Docker example------

docker network ls

docker network create mongo-network

docker run -p 27017:27017 -d -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --net mongo-network mongo

docker logs 8dc1c3b25526ccc251775ddff7976421a85dc9a2891479944258260b152df206

docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --net mongo-network --name mongo-express2 -e E_CONFIG_MONGODB_SERVER=mongodb  mongo-express


docker logs c176b2bf3bbad0099b2cdf37ee7b8252797d5ff10c6d6953add1d54b39c6025c


Docker compose

docker-compose -f docker-mongo.yaml up

https://jsonformatter.org/yaml-formatter

When we restart the container everything that we configure is gone like db and data this could be overturned with docker volumes for persistence

docker-compose -f docker-mongo.yaml down removes the containers and the network



