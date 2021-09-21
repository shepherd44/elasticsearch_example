# Single Node Cluster

## start with docker command

```script
docker run -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.14.2
```

```script
curl -X GET "localhost:9200/_cat/nodes?v=true&pretty"
```

## start with docker-compose

### start

```script
docker-compose up -d
```

### stop

```script
docker-compose stop
```
