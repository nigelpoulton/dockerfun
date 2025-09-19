FROM node:current-alpine

LABEL org.opencontainers.image.authors="@nigelpoulton"

RUN mkdir -p /usr/src/app

COPY . /usr/src/app

WORKDIR /usr/src/app

RUN npm install

ENTRYPOINT [ "node", "app.js" ]
