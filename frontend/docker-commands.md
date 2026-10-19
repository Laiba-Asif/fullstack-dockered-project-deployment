<!-- to build docker file -->
docker build -t frontend --build-arg REACT_APP_API_BASE_URL=http://localhost:3500 .

<!-- to run this build  -->
docker run -d \
  --name frontend-container \
  --network three-tier-network \
  -p 8082:80 \
  frontend

  <!-- docker build --no-cache -t frontend:latest \
  --build-arg REACT_APP_API_BASE_URL=/api \
  -f frontend/Dockerfile frontend/ -->