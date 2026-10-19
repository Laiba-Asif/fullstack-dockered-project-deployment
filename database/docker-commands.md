<!-- DOCKER COMMANDS FOR MY SQL DATABASE -->

<!-- to create network -->
docker network create three-tiernetwork

<!-- to see all networks -->
docker network ls

<!-- to see all volumes -->
docker volume ls

<!-- to create volume -->
docker volume create <volume name> // docker volume create mysql-data

<!-- to build an image -->
docker build -t mysql-image database/

<!-- to run container of this image -->
docker run --name mysql-container -d -p 3306:3306 --network  three-tier-network  -v mysql-data:/var/lib/mysql mysql 

-d = detached mode 
-p = port 
-v = volumes
--name = gives name of container
--network = give name of network

<!-- to check running containers -->
docker ps

<!-- to check logs of container -->
docker logs <container id>

<!-- start docker container  -->
docker start mysql-container
