# build image:
# docker build -t gobuilder <path/to/Dockerfile>
# 
# build go project:
# cd /path/to/project
# docker run --rm -v ${PWD}/bin:/bin gobuilder
FROM golang:alpine3.20 AS builder
RUN mkdir /app
RUN mkdir /bin
WORKDIR /app
COPY . .
RUN go mod tidy
RUN GOOS=linux GOARCH=amd64 go build -o /bin/app-linux-amd64 . 
# assuming main.go in root