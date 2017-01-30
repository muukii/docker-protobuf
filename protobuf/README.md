# Protocol Buffer on Docker

[![Docker Stars](https://img.shields.io/docker/stars/kaneshin/protobuf.svg)](https://hub.docker.com/r/kaneshin/protobuf/)
[![Docker Pulls](https://img.shields.io/docker/pulls/kaneshin/protobuf.svg)](https://hub.docker.com/r/kaneshin/protobuf/)
[![Docker Automated buil](https://img.shields.io/docker/automated/kaneshin/protobuf.svg)](https://hub.docker.com/r/kaneshin/protobuf/)

## Usage

    # print help message of protoc
    docker run -it --rm kaneshin/protobuf --help

    # execute to output files.
    docker run -it --rm -v $PWD:/proto:rw kaneshin/protobuf *.proto

    # execute to output files by user.
    docker run -it --rm -v $PWD:/proto:rw kaneshin/protobuf -u $(id -u):$(id -g) *.proto

## License

[The MIT License (MIT)](http://kaneshin.mit-license.org/)

## Author

Shintaro Kaneko <kaneshin0120@gmail.com>
