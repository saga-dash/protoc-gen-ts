# protoc-gen-ts

proto -> ts

## Example

your proto files

```
docker run --rm\
 -v $(pwd):$(pwd) -w $(pwd)\
 sagadash/protoc-gen-ts\
 --plugin=protoc-gen-ts=/usr/local/bin/protoc-gen-ts\
 --js_out=import_style=commonjs,binary:models\
 --ts_out=service=true:models -Iproto proto/*.proto
```

google/api and google/protobuf

```
docker run --rm\
 -v $(pwd):$(pwd) -w $(pwd)\
 --entrypoint=""\
 sagadash/protoc-gen-ts\
 sh -c "protoc --plugin=protoc-gen-ts=/usr/local/bin/protoc-gen-ts\
 --js_out=import_style=commonjs,binary:models\
 --ts_out=models -I/protobuf /protobuf/google/**/*.proto"
```

## Refs

* https://github.com/znly/docker-protobuf
  * Delete except TS.
* https://www.npmjs.com/package/ts-protoc-gen
