FROM centos:7.2.1511
MAINTAINER Curtis Mattoon <cmattoon@cmattoon.com>

LABEL license=MIT
LABEL name="Python Tox on Centos 7.2.1511"
LABEL com.cmattoon.base="centos7.2.1511"
LABEL com.cmattoon.version="0.1.0"

RUN yum -y install epel-release && \
    yum -y update \
    && \
    yum -y install \
    python-setuptools \
    python-pip \
    python-wheel \
    python34 \
    python34-setuptools \
    python34-pip \
    && \
    yum clean all

RUN pip install --upgrade pip virtualenv tox

WORKDIR /work
VOLUME ["/work"]

ENTRYPOINT ["/usr/bin/tox"]
