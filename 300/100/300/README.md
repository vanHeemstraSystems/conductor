# 300 - Standalone Server Image

To build and run the server image, without using ```docker-compose```, from the ```docker``` directory execute:

```
$ docker build -t conductor:server -f server/Dockerfile ../
$ docker run -p 8080:8080 -d --name conductor_server conductor:server
```

This builds the image ```conductor:server``` and runs it in a container named ```conductor_server```. The API should now be accessible at ```{{ server_host }}```.

To 'login' to the running container, use the command:

```
$ docker exec -it conductor_server /bin/sh
```
