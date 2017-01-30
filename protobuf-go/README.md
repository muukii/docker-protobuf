# Protocol Buffer for Golang on Docker

[![Docker Stars](https://img.shields.io/docker/stars/kaneshin/protobuf-go.svg)](https://hub.docker.com/r/kaneshin/protobuf-go/)
[![Docker Pulls](https://img.shields.io/docker/pulls/kaneshin/protobuf-go.svg)](https://hub.docker.com/r/kaneshin/protobuf-go/)
[![Docker Automated buil](https://img.shields.io/docker/automated/kaneshin/protobuf-go.svg)](https://hub.docker.com/r/kaneshin/protobuf-go/)

## Usage


    # print help message of protoc
    docker run -it --rm kaneshin/protobuf-go --help

    # execute to output files.
    docker run -it --rm -v $PWD:/proto:rw kaneshin/protobuf-go --go_out=. *.proto

    # execute to output files by user.
    docker run -it --rm -v $PWD:/proto:rw kaneshin/protobuf-go -u $(id -u):$(id -g) --go_out=. *.proto

## License

[The MIT License (MIT)](http://kaneshin.mit-license.org/)

## Author

Shintaro Kaneko <kaneshin0120@gmail.com>
