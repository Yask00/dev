FROM node:6.11.5 
# This is an official image, built by the node.js vendors and validated by Docker 
# to be a high-quality image containing the node 6.11.5 interpreter and basic dependencies.

WORKDIR /usr/src/app
# specify that all subsequent actions should be taken from the directory /usr/src/app 
# in your image filesystem (never the host’s filesystem).
COPY package.json .
# COPY the file package.json from your host to the present location (.) in your image (so in this case, to /usr/src/app/package.json)
RUN npm install
COPY . .
#COPY in the rest of your app’s source code from your host to your image filesystem.

CMD [ "npm", "start" ]

