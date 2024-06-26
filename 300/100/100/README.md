# 100 - Steps

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

[{{ server_host }}](https://docs.conductor-oss.org/devguide/running/%7B%7B%20server_host%20%7D%7D)

<img width="1482" alt="swagger" src="https://github.com/vanHeemstraSystems/conductor/assets/1499433/8cd38d2a-7504-434f-bfda-c711bafe4399">

Conductor UI URL

http://localhost:5000/

<img width="1277" alt="conductorUI" src="https://github.com/vanHeemstraSystems/conductor/assets/1499433/92218600-122a-40e6-885b-e7896ff7b5b5">

## 400 - 4. Exiting Compose

```Ctrl+c``` will exit docker compose.

To ensure images are stopped execute: ```docker-compose down```.
