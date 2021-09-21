# Master Data Cluster

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
docker-compose down
```

## kibana

[kibana](localhost:5601)

## production requirements

### Set vm.max_map_count to at least 262144

* Windows

```script
docker-machine ssh
sudo sysctl -w vm.max_map_count=262144
```

If you use wsl

```script
wsl -d docker-desktop
sysctl -w vm.max_map_count=262144
```

* Linux

```script
sysctl -w vm.max_map_count=262144
```
