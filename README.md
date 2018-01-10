# protoc-gen-ts

proto -> ts

## Example

```
docker run --rm\
 -v $(pwd):$(pwd) -w $(pwd)\
 sagadash/protoc-gen-ts\
 --plugin=protoc-gen-ts=/usr/local/bin/protoc-gen-ts\
 --js_out=import_style=commonjs,binary:models\
 --ts_out=service=true:models -I. proto/*.proto
```

## Refs

* https://github.com/znly/docker-protobuf
  * Delete except TS.
* https://www.npmjs.com/package/ts-protoc-gen
