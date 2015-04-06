# [CloudRunner.I/O](https://my.cloudrunner.io)- enabled images. 

# Supported tags and respective `Dockerfile` links

- [`21`, `latest` (_Dockerfile_)](https://github.com/CloudRunnerIO/docker-scripts/blob/master/docker/fedora/21/Dockerfile)
- [`20` (_Dockerfile_)](https://github.com/CloudRunnerIO/docker-scripts/blob/master/docker/fedora/20/Dockerfile)

---
 To run an instance, pass the following parameters:

# Fedora 20 image:
```
docker run -d -i --env SERVER_ID="SERVER_ADDRESS" --env ORG_ID="ORG-ID" -t cloudrunnerio/fedora:20
```

# Fedora 21 image:
```
docker run -d -i --env SERVER_ID="SERVER_ADDRESS" --env ORG_ID="ORG-ID" -t cloudrunnerio/fedora:21
```
---
Find the SERVER_ADDRESS and ORG_ID in your account in [CloudRunner.I/O](https://my.cloudrunner.io).