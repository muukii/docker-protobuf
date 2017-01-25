```bash
$ docker run -it --rm kaneshin/protobuf-go --help
$ docker run -it --rm -v $PWD:/src:rw kaneshin/protobuf-go --go_out=. *.proto
```
