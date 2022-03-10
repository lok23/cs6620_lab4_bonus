# alpine is to save space. Default space is 917mb!! Using alpine reduces to 142mb
FROM node:14-alpine

WORKDIR /usr/src/app

COPY ./package.json ./
COPY ./yarn.lock ./

RUN yarn install

COPY . .

EXPOSE 5000


CMD [ "index.js" ]