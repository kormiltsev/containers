# Go Builder
Build go project without go installed on host.

## Build image
```bash
docker build -t gobuilder .
```

## Build Go application
```bash
cd /path/to/project
docker run --rm -v ${PWD}/bin:/bin gobuilder
```

## More
The binary file will be saved here: `${PWD}/bin`

Go version `1.23.2`

Image used: [golang:alpine3.20](https://hub.docker.com/layers/library/golang/alpine3.20/images/sha256-d21e934609de95ab75ba852128106ccf95ee7531e8b832b5f3b4e833d47a1ba2?context=explore)