# 100 - Running Conductor Using Docker

Steps

## 100 - 1. Clone the Conductor Code

```   
$ git clone https://github.com/conductor-oss/conductor.git
```

## 200 - 2. Build the Docker Compose

```
$ cd conductor
conductor $ cd docker
docker $ docker-compose build
```

## 300 - 3. Run Docker Compose

```
docker $ docker-compose up
```

Once up and running, you will see the following in your Docker dashboard:

- Elasticsearch
- Conductor UI
- Conductor Server

You can access the UI & Server on your browser to verify that they are running correctly:

Conductor Server URL

{{ server_host }}

