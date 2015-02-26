FROM debian:squeeze

MAINTAINER CloudRunner.IO Dev, dev@cloudrunner.io

RUN apt-get update

RUN apt-get -y install g++ python-dev python-pip m2crypto

RUN mkdir -p /etc/cloudrunner
RUN mkdir -p /opt/cloudrunner
RUN mkdir -p /var/run/sock/cloudrunner/
RUN mkdir -p /var/lib/cloudrunner/

ADD startup /opt/startup
ADD cloudrunner-node.conf /etc/cloudrunner/cloudrunner-node.conf

RUN pip install cloudrunner

RUN cloudrunner-node configure --server 0.0.0.0

RUN cloudrunner-node details

ENTRYPOINT ["/opt/startup"]
