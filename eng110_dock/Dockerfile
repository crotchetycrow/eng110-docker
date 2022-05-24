# Create a docker file to build a customised docker image

# Choose an base image

FROM nginx

# Label the image

LABEL MAINTAINER=JACK

# Migrate/transfer/cp/move data from localhost to our image/container

COPY index.html /usr/share/nginx/html/
COPY main.css /usr/share/nginx/html/

# Expose port 80

EXPOSE 80

# Launch the app/run this command at the end

CMD ["nginx", "-g", "daemon off;"]

