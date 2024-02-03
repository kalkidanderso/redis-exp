Deploying Redis Docker Image to Digital Ocean App

Step 1: Pull Redis Docker Image

     Pull the Redis Docker image from Docker Hub:
     cmd:  docker pull redis:latest

Step 2: Create a Redis Docker Image

    Build a custom Docker image for Redis:
    cmd: docker build -t redis .

Step 3: Tagging the Docker Image

    Tag the Redis Docker image for Digital Ocean Container Registry:
    cmd: docker tag redis:latest registry.digitalocean.com/docker-derp/redis:latest

Step 4: Login to Digital Ocean Container Registry

    Login to Digital Ocean Container Registry using doctl:
    cmd: doctl registry login

Step 5: Push the Docker Image to the Registry

    Push the Redis Docker image to Digital Ocean Container Registry:
    cmd: docker push registry.digitalocean.com/docker-derp/redis:latest
