## grpc-php-gen
This image is used to compile proto files into php stubs

### Installation
```bash
docker pull answerati/grpc-php-gen
```

### Example proto to php compilation inside the container
```bash
PHP_LIB_PATH = ./client/php/lib/
GRPC_PHP_PLUGIN_PATH = /opt/grpc/bin/grpc_php_plugin

mkdir $PHP_LIB_PATH
protoc -I. \
    --php_out=${PHP_LIB_PATH} \
    --grpc_out=${PHP_LIB_PATH} \
    --plugin=protoc-gen-grpc=${GRPC_PHP_PLUGIN_PATH} \
    proto/health/*.proto
```
