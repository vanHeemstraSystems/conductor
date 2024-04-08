# 200 - Alternative Persistence Engines

By default ```docker-compose.yaml```` uses ```config-local.properties```. This configures the ```memory``` database, where data is lost when the server terminates. This configuration is useful for testing or demo only.

A selection of ```docker-compose-*.yaml``` and ```config-*.properties``` files are provided demonstrating the use of alternative persistence engines.

| File | Containers |
| --- | --- |
| docker-compose.yaml | 1. In Memory Conductor Server<br/>2. Elasticsearch<br/>3. UI |
| docker-compose-dynomite.yaml | 1. Conductor Server<br/>2. Elasticsearch<br/>3. UI<br/>4. Dynomite Redis for persistence |
| docker-compose-postgres.yaml | 1. Conductor Server<br/>2. Elasticsearch<br/>3. UI<br/>4. Postgres persistence |
| docker-compose-prometheus.yaml | Brings up Prometheus server |

For example this will start the server instance backed by a PostgreSQL DB.

```
docker-compose -f docker-compose.yaml -f docker-compose-postgres.yaml up
```
