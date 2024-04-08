# 900 - Potential problem when using Docker Images

## Not enough memory
You will need at least 16 GB of memory to run everything. You can modify the docker compose to skip using Elasticsearch if you have no option to run this with your memory options.

To disable Elasticsearch using Docker Compose - follow the steps above.

## Elasticsearch fails to come up in arm64 based CPU machines
As of writing this article, Conductor relies on 6.8.x version of Elasticsearch. This version doesn't have an arm64 based Docker image. You will need to use Elasticsearch 7.x which requires a bit of customization to get up and running

## Elasticsearch remains in Yellow health
When you run Elasticsearch, sometimes the health remains in Yellow state. Conductor server by default requires Green state to run when indexing is enabled. To work around this, you can use the following property: ```conductor.elasticsearch.clusterHealthColor=yellow```

See Github [issue](https://github.com/Netflix/conductor/issues/2262)

## Elasticsearch timeout
Symptom: Standalone (single node) Elasticsearch has a yellow status which will cause timeout for the Conductor server at startup (Required: Green).

Solution: Spin up a cluster (more than one node) to prevent the timeout or use config option ```conductor.elasticsearch.clusterHealthColor=yellow```.

See Github [issue](https://github.com/Netflix/conductor/issues/2262)

## Changes in config-*.properties do not take effect
Config is copied into the image during the docker build. You have to rebuild the image or better, link a volume to it to reflect new changes automatically.

## Unable to access to conductor:server API on port 8080
It may takes some time for conductor server to start. Please check server log for errors.
