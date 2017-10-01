FROM ubuntu:16.04
MAINTAINER Curtis Mattoon <cmattoon@cmattoon.com>

LABEL license=MIT
LABEL name="Python Tox on Ubuntu 16.04"
LABEL com.cmattoon.base="ubuntu16.04"
LABEL com.cmattoon.version="0.1.0"

RUN apt-get -y update && apt-get install -y \
    python \
    python3 \
    python-setuptools \
    python3-setuptools \
    python-pip \
    python3-pip \
    python-wheel \
    && \
    rm -rf /var/lib/apt/lists/*

RUN pip install --upgrade pip virtualenv tox

WORKDIR /work
VOLUME ["/work"]

ENTRYPOINT ["/usr/local/bin/tox"]
