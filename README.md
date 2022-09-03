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