FROM node:alpine
LABEL maintainer="giangoular1994@gmail.com"

WORKDIR /app

COPY ./package.json ./

RUN npm install

COPY . .

CMD [ "npm", "run", "start" ]