Build image
```
docker build -t <image name> . 
```


Run
```shell
docker run \
    -it \
    --rm \
    -v ${PWD}:/app \
    -v /app/node_modules \
    -p 3000:3000 \
    -e CHOKIDAR_USEPOLLING=true \
    <image name>:latest
```
Access to http://localhost:3000