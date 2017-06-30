# Mara

```bash
# Go to here
git clone https://github.com/herereadthis/mara.git
cd mara

# Create the Docker image
docker build -t friendlyhello .

# List the images
docker images

# Run the app
docker run -p 4000:80 friendlyhello

# View the app at http://localhost:4000/
# Or view the content from inside terminal
curl http://localhost:4000/

# Quit.
# Run the app in the background, in detached mode.
docker run -d -p 4000:80 friendlyhello

# List the container
docker ps

# Login
docker login

# Tag the image
docker tag friendlyhello herereadthis/mara:part1
docker images

# Publish the image: upload tagged image to repository
docker push herereadthis/mara:part1

# Pull and run the image from the remote repository
docker run -p 4000:80 herereadthis/mara:part1
```

```bash
# Services

# Start the swarm
docker swarm init

docker stack deploy -c docker-compose.yml helloworld2

docker stack ps helloworld2

# go to localhost
# each time you refresh, the container ID will be different
```
