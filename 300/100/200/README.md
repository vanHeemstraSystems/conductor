# 200 - Alternative Persistence Engines

By default ```docker-compose.yaml```` uses ```config-local.properties```. This configures the ```memory``` database, where data is lost when the server terminates. This configuration is useful for testing or demo only.

A selection of ```docker-compose-*.yaml``` and ```config-*.properties``` files are provided demonstrating the use of alternative persistence engines.

| File | Containers |
| --- | --- |
| docker-compose.yaml | 1. In Memory Conductor Server<br/>2. Elasticsearch<br/>3. UI |
| ... | ... |
