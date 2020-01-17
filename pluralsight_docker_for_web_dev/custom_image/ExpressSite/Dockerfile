FROM node:latest

MAINTAINER Yasen Trayanov

ENV NODE_ENV=production
ENV PORT=3000

COPY . /var/www
# bake the src code as file layer into that layered file system docker build for images

WORKDIR /var/www

RUN ls -la
RUN npm install

# VOLUME ["/var/www"]
# that is gonna cause docker once when the container runs to mount this volume 
# in the container into folder at the  host file system

EXPOSE $PORT 
# image and container to run on 3000

ENTRYPOINT ["npm", "start"]
#when the container is started what is the entry point
