# hbase-standalone

## Usage
```
docker run -it \
        -p 8080:8080 \
        -p 9090:9090 \
        -p 2181:2181 \
        -p 16000:16000 \
        -p 16010:16010 \
        -p 16020:16020 \
        -p 16030:16030 \
      hbase-standalone:2.1.2
```

#### HBase Master server interface
http://localhost:16010/master-status

#### Verifying HBase REST interface
```
# HBase Version
[user@host ~]$ curl http://localhost:8080/version/cluster

# Cluster Status
[user@host ~]$ curl http://localhost:8080/status/cluster

# Table List
[user@host ~]$ curl http://localhost:8080/
```
### Accessing the HBase shell
```
[user@host ~]$ docker exec -it hbase bash
user@host:/opt# hbase shell
```

## Build it

```
docker build -t hbase-standalone:2.1.2 .
```