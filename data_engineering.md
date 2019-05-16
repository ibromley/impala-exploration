# Data Engineering Exploration

### Using Cloudera's quickstart VM

I spun up a host on Digital Ocean with docker to run the `cloudera/quickstart` image. On the host I ran these commands
```
docker pull cloudera/quickstart:latest
scp ~/trainings/.... -> droplet root
docker run --hostname=quickstart.cloudera --privileged=true -t -i \
-v /root:/data --publish-all=true \
-p 8888:8888 -p 80:80 -p 7180:7180 -p 50070:50070 \
cloudera/quickstart /usr/bin/docker-quickstart
```
Additional exercises should be in the respective folders.
