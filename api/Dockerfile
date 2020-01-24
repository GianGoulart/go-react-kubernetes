FROM golang:1.12

ENV GO111MODULE=on

WORKDIR /app

COPY ./go.mod .

RUN go mod download

COPY . .
CMD ["go", "run", "main.go"]