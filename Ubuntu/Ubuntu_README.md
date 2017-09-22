# Ubuntu DockerDev

### To build Ubuntu docker-dev image locally
```
docker build --rm -t github/ubuntu-dockerdev /Users/sharmava/Github/DockerDev/Ubuntu
```
Note that dir ```/Users/sharmava/Github/DockerDev/Ubuntu``` is where my Dockerfile is present.

### To run the local image
```
docker run -it -v /Users:/Users github/ubuntu-dockerdev /bin/bash
```
Note that I've mounted /Users directory here. You should choose the directory where your code is present.
