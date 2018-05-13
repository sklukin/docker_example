# specify the node base image with your desired version node:<version>
FROM node:8

WORKDIR /opt/app

COPY ../spa /opt/app

RUN npm install

RUN npm run build

# replace this with your application's default port
EXPOSE 8888
