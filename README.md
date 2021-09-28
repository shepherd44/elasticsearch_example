# elasticsearch examples

## docker example list

### ELK Stack

single-node-elk

```script
pwd=$(pwd)
cd $pwd/single-node-elk
ELK_VERSION=7.14.2 docker-compose up -d
```

### Beat Example

single-node-elk + beats

```script
pwd=$(pwd)
cd $pwd/single-node-elk
ELK_VERSION=7.14.2 docker-compose up -d
cd $pwd/beats
ELK_VERSION=7.14.2 docker-compose up -d
```
