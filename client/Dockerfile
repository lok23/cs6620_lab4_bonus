# alpine is to save space. Default space is 917mb!! Using alpine reduces to 478mb
FROM node:14-alpine

WORKDIR /usr/src/app

COPY ./package.json ./
COPY ./yarn.lock ./

RUN yarn install

COPY . .

EXPOSE 3000

#Tried to further reduce size by using multi-step build, but couldn't figure out which distro was best
#FROM alpine:3.12
#COPY --from=build /usr/src/app /usr/src/app
#WORKDIR /app
CMD [ "yarn", "start" ]