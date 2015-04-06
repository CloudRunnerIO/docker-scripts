# [CloudRunner.I/O](https://my.cloudrunner.io)- enabled images. 

# Supported tags and respective `Dockerfile` links

- [`jessie`, `latest` (_Dockerfile_)](https://github.com/CloudRunnerIO/docker-scripts/blob/master/docker/debian/jessie/Dockerfile)
- [`wheezy` (_Dockerfile_)](https://github.com/CloudRunnerIO/docker-scripts/blob/master/docker/debian/wheezy/Dockerfile)
- [`squeeze` (_Dockerfile_)](https://github.com/CloudRunnerIO/docker-scripts/blob/master/docker/debian/squeeze/Dockerfile)

---
 To run an instance, pass the following parameters:

# Squeeze image:
```
docker run -d -i --env SERVER_ID="SERVER_ADDRESS" --env ORG_ID="ORG-ID" -t cloudrunnerio/debian:squeeze
```

# Wheezy image:
```
docker run -d -i --env SERVER_ID="SERVER_ADDRESS" --env ORG_ID="ORG-ID" -t cloudrunnerio/debian:wheezy
```

# Jessie image:
```
docker run -d -i --env SERVER_ID="SERVER_ADDRESS" --env ORG_ID="ORG-ID" -t cloudrunnerio/debian:jessie
```
---
Find the SERVER_ADDRESS and ORG_ID in your account in [CloudRunner.I/O](https://my.cloudrunner.io).