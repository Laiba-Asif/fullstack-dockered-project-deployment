<!-- to make backend build and create backend image-->
docker build -t backend backend 
<!-- first backend is build name and 2nd is backend folder  -->

<!-- to list images -->
docker images

<!-- to run backend image -->
docker run -d -p 3500:3500 --network three-tier-network --name backend-container backend

