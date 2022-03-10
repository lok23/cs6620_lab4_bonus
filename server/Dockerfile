# alpine is to save space. Default space is 917mb!! Using alpine reduces to 142mb
FROM node:14-alpine

# set the work directory
WORKDIR /usr/src/app

# first copy only the packages we will use to the work directory
COPY ./package.json ./
COPY ./yarn.lock ./

# install said packages
RUN yarn install

# copy everything else
COPY . .

# expose port 5000 for connections
EXPOSE 5000

# run server's index.js file
CMD [ "index.js" ]