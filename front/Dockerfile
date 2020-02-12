FROM node:alpine
LABEL maintainer="giangoular1994@gmail.com"

WORKDIR /app

COPY ./package.json /app/

RUN npm install

COPY ./ /app/

RUN npm run build

# Stage 1, based on Nginx, to have only the compiled app, ready for production with Nginx
FROM nginx:1.15
COPY  /app/build/ /usr/share/nginx/html 
