FROM mongo

LABEL MAINTAINER=JACK

COPY . .

RUN   sed -i "s|bindIp: 127.0.0.1|bindIp: 0.0.0.0|g" /etc/mongod.conf.orig

EXPOSE 27017