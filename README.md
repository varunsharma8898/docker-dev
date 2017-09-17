# DockerDev
Docker with Perl, Python3, MariaDB and a few other useful packages - to quick start development without worrying about seting up environment and dependencies.

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

### CentOS
Check out [CentOS_README](CentOS/CentOS_README.md) on how to build and run a docker-dev image based on CentOS.

### MariaDB
Check out [MariaDB_README.md](MariaDB/MariaDB_README.md) on how to set up mariaDB in a docker container and access it from docker-dev.