FROM centos:latest

ENV TESTENV your-test-environment

RUN yum -y update && \
    yum -y install yum-utils && \
    yum -y groupinstall development && \
    yum -y install https://centos7.iuscommunity.org/ius-release.rpm && \
    yum -y install python36u \
        python36u-pip \
        perl-CPAN && \
    cpan -i CPAN && \
    cpan -i Net::SFTP::Foreign \
     STEVENL/Test-Mocha-0.61.tar.gz \
     Test::Unit::Lite \
     REST::Client && \
    yum clean all



