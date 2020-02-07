FROM node:alpine
LABEL maintainer="giangoular1994@gmail.com"

WORKDIR /front/src

COPY ./package.json ./

RUN npm install

COPY . .

RUN npm run build

# Stage 1, based on Nginx, to have only the compiled app, ready for production with Nginx
FROM nginx:1.15
COPY --from=build /front/build/ /usr/share/nginx/html 
EXPOSE 80