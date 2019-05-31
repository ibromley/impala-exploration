# Data Engineering Exploration

### Using Cloudera's quickstart VM

I spun up a host on Digital Ocean with docker to run the `cloudera/quickstart` image. On the host I ran these commands
```
docker pull cloudera/quickstart:latest
scp ~/trainings/.... -> droplet root
docker run --hostname=quickstart.cloudera --privileged=true -t -i \
-v /root:/data --publish-all=true \
-p 8888:8888 -p 80:80 -p 7180:7180 -p 50070:50070 \
-p 8983:8983 -p 8088:8088 -p 11000:11000 -p 9092:9092 \
cloudera/quickstart /usr/bin/docker-quickstart
```
Additional exercises should be in the respective folders.

|Port | Service |
|---------|------|
| 8888  | [Hue](http://quickstart.cloudera:8888/) |
| 7180  | [Cloudera Manager](http://quickstart.cloudera:7180/) |
| 80    | [Tutorial](http://quickstart.cloudera:80/) |
| 8983  | [SolR](http://quickstart.cloudera:8983/solr) |
| 8088  | [Hadoop MapReduce UI](http://quickstart.cloudera:8088)
| 11000 | [Oozie](http://quickstart.cloudera:11000/)
| 9092  | Kafka 
| 2181  | Zookeeper
