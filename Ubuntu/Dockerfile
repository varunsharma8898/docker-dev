FROM phusion/baseimage:0.9.22

# Install packages
RUN apt-get update -qq

RUN apt-get -qqy install \
    libdbd-mysql-perl \
    mlocate \
    mysql-client \
    python3-pymysql \
    vim

RUN apt-get -qqy install \
    build-essential

RUN updatedb
