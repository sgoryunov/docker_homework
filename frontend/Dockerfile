FROM node:14-alpine as builder
WORKDIR /usr/src/app
COPY . .
RUN apk add --no-cache bash curl
RUN npm install && npm run build 
RUN npm install -g serve
EXPOSE 3000
CMD [ "serve", "-s", "build" ]