`docker run hello-world` - Runs the image named 'hello-world'
Looks in local host then looks in registry

`docker run -d -p 80:80 nginx` - '-d' for detached, '-p' for port

`docker run -d -p 90:80 nginx` - map port 80 to port 90

`docker ps` - show running image, `docker ps -a` for all images

`docker images` - shows all available images

`docker exec -it 'container ID' sh` - enters the shell inside the container

`docker run -d -p 4000:4000 docs/docker.github.io` - dockers documentation

`docker stop 'container ID'` - Stop that image

`docker rm 'container ID'` - Removes that image from local

`docker tag nginx repo-name/tag-name:latest` - Tags the image to your desired repository

`docker commit container-ID acc-name/repo-name:tag-name` - Commits the image

`docker push acc-name/repo-name:tag-name` - Push the image to the repository

`docker login` - Logs into docker from the terminal

`docker logs 'container ID'` - displays the logs for the container
