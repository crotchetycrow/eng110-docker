# Setting up a node.js app image with docker

`nano Dockerfile` - create a Dockerfile

```

# Create a docker file to build a customised docker image

# Choose an base image

FROM node

# Label the image

LABEL MAINTAINER=JACK

# Migrate/transfer/cp/move data from localhost to our image/container

WORKDIR /usr/src/app

COPY app/ /usr/src/app/

# Install NPM

RUN npm install -g npm@latest

RUN npm install express

COPY . .

# Expose port 3000

EXPOSE 3000

# Launch the app/run this command at the end

CMD ["node", "app.js"]
```

`docker build -t repo-name/tag-name:v2 .` - builds the image

`docker run -d -p 3000:3000 repo-name/tag:v2` - runs the image specified on port 3000

### Refactor code with the following to get it ready for production

```
# Create a docker file to build a customised docker image

# Choose an base image

FROM node AS app

# Label the image

LABEL MAINTAINER=JACK

# Migrate/transfer/cp/move data from localhost to our image/container

WORKDIR /usr/src/app

COPY app/ /usr/src/app/

# Install NPM

RUN npm install -g npm@latest

RUN npm install express

COPY . .

# Expose port 3000

EXPOSE 3000

# Launch the app/run this command at the end

CMD ["node", "app.js"]

# ####

FROM node:alpine

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install -g npm@latest

RUN npm install express

# This line of code does the magic here to compress the images
COPY --from=app /usr/src/app /usr/src/app

EXPOSE 3000

CMD ["node", "app.js"]
```

`docker build -t repo-name/tag-name .` - builds the image
