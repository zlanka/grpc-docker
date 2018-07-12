## grpc-go-gen
This image is used to compile proto files into go stubs

### Installation
```bash
docker pull answerati/grpc-go-gen
```

### Example proto to go compilation inside the container
```bash
protoc -I. \
    --plugin=protoc-gen-grpc \
    --go_out=plugins=grpc,paths=source_relative:. \
    proto/health/*.proto
```
