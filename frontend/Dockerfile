FROM node:12-alpine as builder
WORKDIR /usr/src/app
COPY . .
RUN apk add --no-cache bash
RUN npm install
EXPOSE 3000
# RUN npm run build
ENTRYPOINT [ "npm", "start" ]
#CMD [ "bash" ]
# FROM nginx:1.21-alpine
# RUN apk add --no-cache bash
# COPY --from=builder /usr/src/app/build/* /usr/share/nginx/html/
# COPY --from=builder /usr/src/app/node_modules /usr/share/nginx/html/node_modules