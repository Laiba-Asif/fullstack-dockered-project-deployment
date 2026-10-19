<!-- to build docker file -->
docker build -t frontend --build-arg REACT_APP_API_BASE_URL=localhost:3500 frontend/

<!-- to run this build  -->
docker run -d --name frontend-container --network three-tier-network -p 80:3000 frontend/