
# Create a docker file to build a customised docker image

# Choose an base image

FROM node

# Label the image

LABEL MAINTAINER=JACK

# Migrate/transfer/cp/move data from localhost to our image/container

WORKDIR /app

COPY ["package.json", "package*.json", "./"]

# Install NPM

RUN npm install

COPY . .

# Expose port 3000

EXPOSE 3000

# Launch the app/run this command at the end

CMD ["node", "app.js"]