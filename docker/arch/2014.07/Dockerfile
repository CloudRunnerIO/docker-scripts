FROM base/archlinux

MAINTAINER CloudRunner.IO Dev, dev@cloudrunner.io

RUN pacman -Syu --noconfirm

RUN pacman -Sy --noconfirm wget python2 python2-pip swig gcc openssl python2-setuptools

RUN mkdir -p /etc/cloudrunner
RUN mkdir -p /opt/cloudrunner
RUN mkdir -p /var/run/sock/cloudrunner/
RUN mkdir -p /var/lib/cloudrunner/

ADD startup /opt/startup
ADD cloudrunner-node.conf /etc/cloudrunner/cloudrunner-node.conf

RUN wget --no-cache -O - https://raw.githubusercontent.com/CloudRunnerIO/cloudrunner-library/master/bootstrap.sh | \
   CRN_NORUN=1 CRN_SERVER=0.0.0.0 /bin/bash

ENTRYPOINT ["/opt/startup"]

