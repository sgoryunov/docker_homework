FROM node:16-alpine
WORKDIR /usr/src/app
COPY . .
RUN apk add --no-cache bash
RUN npm install
USER node
CMD npm start