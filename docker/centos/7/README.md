# [CloudRunner.I/O](https://my.cloudrunner.io)- enabled images.

# Supported tags and respective `Dockerfile` links

- [`latest`, `centos7` (_Dockerfile_)](https://github.com/CloudRunnerIO/docker-scripts/blob/master/docker/centos/7/Dockerfile)
- [`centos6` (_Dockerfile_)](https://github.com/CloudRunnerIO/docker-scripts/blob/master/docker/centos/6/Dockerfile)

---
 To run an instance, pass the following parameters:

# Centos 6 image:
```
docker run -d -i --env SERVER_ID="SERVER_ADDRESS" --env ORG_ID="ORG-ID" -t cloudrunnerio/centos:centos6
```

# Centos 7 image
```
docker run -d -i --env SERVER_ID="SERVER_ADDRESS" --env ORG_ID="ORG-ID" -t cloudrunnerio/centos:centos7
```
---
Find the SERVER_ADDRESS and ORG_ID in your account in [CloudRunner.I/O](https://my.cloudrunner.io).