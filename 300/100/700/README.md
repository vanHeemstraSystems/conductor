# 700 - Elasticsearch

Elasticsearch is optional, please be aware that disable it will make most of the conductor UI not functional.

How to enable Elasticsearch
- Set ```conductor.indexing.enabled=true``` in ```your_config.properties```
- Add config related to elasticsearch E.g.: ```conductor.elasticsearch.url=http://es:9200```

How to disable Elasticsearch
- Set ```conductor.indexing.enabled=false``` in ```your_config.properties```
- Comment out all the config related to elasticsearch E.g.: ```conductor.elasticsearch.url=http://es:9200```
