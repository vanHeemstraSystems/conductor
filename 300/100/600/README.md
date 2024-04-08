# 600 - Combined Server & UI Docker Image

This image at ```/docker/serverAndUI``` is provided to illustrate starting both the server & UI within the same container. The UI is hosted using nginx.

Building the combined image

From the ```docker``` directory,

```
$ docker build -t conductor:serverAndUI -f serverAndUI/Dockerfile ../
```

Running the combined image

- With interal DB: ```$ docker run -p 8080:8080 -p 80:5000 -d -t conductor:serverAndUI```
- With external DB: ```$ docker run -p 8080:8080 -p 80:5000 -d -t -e "CONFIG_PROP=config.properties" conductor:serverAndUI```
