FROM debian:jessie

MAINTAINER CloudRunner.IO Dev, dev@cloudrunner.io

RUN apt-get update

RUN apt-get -y install wget g++ python-dev python-pip swig libssl-dev m2crypto msgpack-python ca-certificates

RUN mkdir -p /etc/cloudrunner
RUN mkdir -p /opt/cloudrunner
RUN mkdir -p /var/run/sock/cloudrunner/
RUN mkdir -p /var/lib/cloudrunner/

ADD startup /opt/startup
ADD cloudrunner-node.conf /etc/cloudrunner/cloudrunner-node.conf

RUN wget --no-cache -O - https://raw.githubusercontent.com/CloudRunnerIO/cloudrunner-library/master/bootstrap.sh | \
   CRN_NORUN=1 CRN_SERVER=0.0.0.0 /bin/bash

ENTRYPOINT ["/opt/startup"]
