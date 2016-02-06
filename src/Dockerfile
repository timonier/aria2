FROM alpine:3.1
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    ARIA2_VERSION=1.18.8 \
    CA_CERTIFICATES_VERSION=20141019

RUN set -x \

    # Prepare system

    && resolve() { echo $(apk search $1 | grep "$1-$2" | sed -e "s/$1-/$1=/g") ; } \
    && apk add -U \

    # Install packages

    && apk add \
           $(resolve aria2 $ARIA2_VERSION) \
           $(resolve ca-certificates $CA_CERTIFICATES_VERSION) \

    # Clean

    && rm -rf \
           /var/cache/apk/*

ENTRYPOINT [ "/usr/bin/aria2c" ]
