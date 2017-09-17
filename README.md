# docker-dev
Docker with Perl, Python3 and a few useful packages - to quick start development without worrying about seting up environment and dependencies.

## Prerequisites
Boot2Docker
or Docker-machine

This was built using boot2docker. However it is recommended to migrate to docker-machine.

Check out [this page](https://docs.docker.com/machine/migrate-to-machine/) to migrate from boot2docker to docker-machine.

## Getting Started

### To start boot2docker
```
boot2docker up
$(boot2docker shellinit)
```

### To build docker-dev image locally
```
docker build --rm -t github/docker-dev /Users/sharmava/Github/DockerDev/CentOS
```

### To run the local image
```
docker run -it -v /Users:/Users github/docker-dev /bin/bash
```
Note that I've mounted /Users directory here. You should choose a different directory where your code is present.
