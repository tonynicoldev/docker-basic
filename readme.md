# Intro to Docker and Docker Compose
This demo is super simple code as the code isn't important here as the objective is to demonstrate how to create Docker images and containers

The code has a single endpoint which simply returns a parsed version of the http request

.rest has urls to access the endpoint in the app at 3000 and access the app via the container at the container port 4000

## Basic commands


**docker build .**  Creates an image with no name  
**docker images -a**  -a needed to show all images including those with no name  
**docker build . -t demo:v1**  Create an image with a name demo1:v1  
**docker images**  Show images with a name - no need for -a  
**docker run -d -p 4000:3000 --name test --rm demo:v1**  --rm deletes test container when stopped  
**docker ps**  Shows the running containers  
**docker stop test**  Stop the test container and delete it if --rm was used before  

**docker compose build**  Builds the image based on the compose.yaml and Dockerfile  
**docker compose up**  Starts the container referenced in the compose file - in the foreground  
**docker compose up -d** Starts the container in the background enabling terminal access  
**docker compose down**  Stop and delete the container  
**docker compose up -d --build**  Build the image before starting it as a container  
