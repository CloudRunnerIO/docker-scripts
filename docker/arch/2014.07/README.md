# [CloudRunner.I/O](https://my.cloudrunner.io)- enabled images. 

# Supported tags and respective `Dockerfile` links

- [`2014.07`, `latest` (_Dockerfile_)](https://github.com/CloudRunnerIO/docker-scripts/blob/master/docker/arch/2014.07/Dockerfile)
- [`2014.01` (_Dockerfile_)](https://github.com/CloudRunnerIO/docker-scripts/blob/master/docker/arch/2014.01/Dockerfile)

---
 To run an instance, pass the following parameters:

# ArchLinux 2014.01:
```
docker run -d -i --env SERVER_ID="SERVER_ADDRESS" --env ORG_ID="ORG-ID" -t cloudrunnerio/arch:2014.01
```

# ArchLinux 2014.07:
```
docker run -d -i --env SERVER_ID="SERVER_ADDRESS" --env ORG_ID="ORG-ID" -t cloudrunnerio/arch:2014.07
```
---
Find the SERVER_ADDRESS and ORG_ID in your account in [CloudRunner.I/O](https://my.cloudrunner.io).