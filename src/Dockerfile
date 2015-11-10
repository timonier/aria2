FROM alpine:3.1
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    ARIA2_VERSION=1.18.8-r0 \
    CA_CERTIFICATES_VERSION=20141019-r0

RUN set -x \
    && apk add -U aria2=$ARIA2_VERSION ca-certificates=$CA_CERTIFICATES_VERSION \
    && rm -rf /var/cache/apk/*

ENTRYPOINT [ "/usr/bin/aria2c" ]
