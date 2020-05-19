# hugo-extended-docker

Docker image for building sites that need Hugo extended

Uses `ubuntu:latest` as base image and adds the following:

- Go 1.14
- NodeJS 12.x.x
- Hugo extended 0.65.3

## Build

```sh
export HUGO_VERSION=$(cat HUGO_VERSION)
docker build . -t hugo-extended:$HUGO_VERSION --build-arg HUGO_VERSION=$HUGO_VERSION
docker build . -t hugo-extended:latest --build-arg HUGO_VERSION=$HUGO_VERSION
```

## Run

`docker run -it -v ${PWD}:/WORKDIR hugo:latest bash`