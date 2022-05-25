# Setting up a mongodb image with docker

`nano Dockerfile` - create a Dockerfile

```
FROM mongo

LABEL MAINTAINER=JACK

COPY . .

RUN   sed -i "s|bindIp: 127.0.0.1|bindIp: 0.0.0.0|g" /etc/mongod.conf.orig

EXPOSE 27017
```

`docker build -t repo-name/tag-name:v2 .` - builds the image

`docker run -d -p 27017:27017 repo-name/tag:v2` - runs the image specified on port 27017

## Connecting containers together

### Create a docker-compose yml file

```
version: "3"
services:

  mongodb:
    # Name of the container
    container_name: container-ID
    # Base image being used
    image: mongo
    # restart: always
    # Makes the data from this path persistent
    volumes:
      - ~/mongo:/data/db
    # The port that mongodb will be on
    ports:
      - "27017:27017"

  nodeapp:
    container_name: container-ID
    # Restarts the container in the event of failure
    restart: always
    # The build that you want to use with this app
    build:
      context: .
      dockerfile: Dockerfile
    # Sets the environment that it needs to connect to
    environment:
      - DB_HOST=mongodb://mongodb:27017/posts
    # The port that the app will be on
    ports:
      - "80:3000"
    # What container app is linking to
    links:
      - mongodb
```

`docker-compose up -d` - runs the .yml file in a detached state

`docker-compose down` - shuts down the running containers
