# docker build -t goav3 .
# cd /path/to/project
# docker run -v $PWD:/goa --rm goav3 goa gen github.com/kormiltsev/backend/api/design -o ./api
FROM golang:1.22-alpine3.19

WORKDIR /goa

RUN go install goa.design/goa/v3/cmd/goa@v3
RUN go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
RUN go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest 