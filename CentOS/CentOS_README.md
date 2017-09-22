# CentOS DockerDev

### To build CentOS docker-dev image locally
```
docker build --rm -t github/vsharma-dockerdev /Users/sharmava/Github/DockerDev/CentOS
```
Note that dir ```/Users/sharmava/Github/DockerDev/CentOS``` is where my Dockerfile is present.

### To run the local image
```
docker run -it -v /Users:/Users github/vsharma-dockerdev /bin/bash
```
Note that I've mounted /Users directory here. You should choose the directory where your code is present.
