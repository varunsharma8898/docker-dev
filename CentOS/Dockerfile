FROM centos:latest

ENV TESTENV your-test-environment

# Installing yum utils and development tools separately
# as I dont need these to be at their latest always
# and I can use the image in cache to build quickly.
RUN yum -y update && \
    yum -y install yum-utils && \
    yum -y groupinstall development && \
    yum -y install https://centos7.iuscommunity.org/ius-release.rpm

# All the yum-install packages should ideally be in a single RUN command
# But separating this out from the above
# to make the build quick and debug any issues with it.
RUN yum -y install python36u \
        python36u-pip \
        perl-CPAN \
        mysql \
        "perl(DBD::mysql)" \
        mlocate \
        vim && \
        yum clean all

# Install libs from Perl and Python here
#RUN cpan -i Net::SFTP::Foreign \
#        STEVENL/Test-Mocha-0.64.tar.gz \
#        Test::Unit::Lite \
#        REST::Client

RUN updatedb
