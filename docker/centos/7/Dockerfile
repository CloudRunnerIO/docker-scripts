FROM centos:centos7

MAINTAINER CloudRunner.IO Dev, dev@cloudrunner.io

RUN yum -Cy install epel-release
RUN yum makecache
RUN yum update -Cy
RUN yum -Cy install python-zmq python-pip m2crypto python-msgpack python-psutil

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
