FROM debian:squeeze

MAINTAINER CloudRunner.IO Dev, dev@cloudrunner.io

RUN apt-get update

RUN apt-get -y install wget g++ python-dev python-pip swig libssl-dev m2crypto curl

RUN mkdir -p /etc/cloudrunner
RUN mkdir -p /opt/cloudrunner
RUN mkdir -p /var/run/sock/cloudrunner/
RUN mkdir -p /var/lib/cloudrunner/

ADD startup /opt/startup
ADD cloudrunner-node.conf /etc/cloudrunner/cloudrunner-node.conf

RUN curl -o bootstrap.sh https://raw.githubusercontent.com/CloudRunnerIO/cloudrunner-library/master/bootstrap.sh
RUN CRN_NORUN=1 CRN_SERVER=0.0.0.0 /bin/bash bootstrap.sh

ENTRYPOINT ["/opt/startup"]
