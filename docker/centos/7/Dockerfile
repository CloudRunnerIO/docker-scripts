FROM centos:centos7

MAINTAINER CloudRunner.IO Dev, dev@cloudrunner.io

RUN yum update -y

RUN yum -y install epel-release

RUN yum -y install wget python-devel swig gcc-c++ openssl-devel vim htop openssh rpm-build make python-setuptools git-core m2crypto python-msgpack openssl

RUN mkdir -p /etc/cloudrunner
RUN mkdir -p /opt/cloudrunner
RUN mkdir -p /var/run/sock/cloudrunner/
RUN mkdir -p /var/lib/cloudrunner/

ADD startup /opt/startup
ADD cloudrunner-node.conf /etc/cloudrunner/cloudrunner-node.conf

RUN wget --no-cache -O - https://raw.githubusercontent.com/CloudRunnerIO/cloudrunner-library/master/bootstrap.sh | \
   CRN_NORUN=1 CRN_SERVER=0.0.0.0 /bin/bash

ENTRYPOINT ["/opt/startup"]
