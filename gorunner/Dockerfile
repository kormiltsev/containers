FROM golang:alpine3.20 AS builder
RUN mkdir /app
WORKDIR /app
COPY . .
RUN go mod tidy

RUN GOOS=linux GOARCH=amd64 go build -o ./application
 
FROM alpine:3.20.0
WORKDIR /
COPY --from=builder /app/application .
# make some actions/preparations here

CMD ["/application"]