FROM node:14-alpine as builder
WORKDIR /usr/src/app
COPY . .
#RUN apk add --no-cache bash
RUN npm install && npm run build 
RUN npm install -g serve
CMD [ "serve", "-s", "build" ]
#CMD [ "bash" ]
# FROM nginx:1.21-alpine
# RUN apk add --no-cache bash
# COPY --from=builder /usr/src/app/build/* /usr/share/nginx/html/
# CMD ["nginx", "-g", "daemon off;"]
