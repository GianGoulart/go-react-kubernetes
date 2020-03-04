FROM golang:1.12-alpine
LABEL maintainer="giangoular1994@gmail.com"

ENV GO111MODULE=on

WORKDIR /api

COPY ./go.mod .

RUN go mod download

COPY . .

CMD ["go", "run", "main.go"]