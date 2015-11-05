FROM debian:jessie
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    DEBIAN_FRONTEND=noninteractive \
    ARIA2_VERSION=1.18.8

RUN set -x \
    && apt-get update \
    && apt-get install -y --no-install-recommends aria2=$ARIA2_VERSION* ca-certificates \
    && rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "/usr/bin/aria2c" ]
