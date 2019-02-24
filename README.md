# Impala Exploration

### Using Cloudera's quickstart VM

I spun up a host on Digital Ocean with docker to run the `cloudera/quickstart` image. On the host I ran these commands
```
docker pull cloudera/quickstart:latest
git clone https://resources.oreilly.com/examples/0636920049562.git
mv 0636920049562/ impala-course/
docker run --hostname=quickstart.cloudera --privileged=true -t -i \
-v /root:/src --publish-all=true -p 8888:8888 -p 80:80 -p 7180:7180 \
cloudera/quickstart /usr/bin/docker-quickstart
```
Additional exercises should be in the respective folders.
