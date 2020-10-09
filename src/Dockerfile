FROM alpine:latest

LABEL \
    maintainer="Morgan AUCHEDE <morgan.auchede@gmail.com>"

RUN set -e -u -x \
\
    # Install packages
\
    && apk add --no-cache --no-progress --virtual BUILD_DEPS build-base c-ares-dev curl expat-dev gnutls-dev sqlite-dev \
    && apk add --no-cache --no-progress bash c-ares ca-certificates expat libstdc++ sqlite-libs gnutls tzdata \
\
    # Install aria2
\
    && curl --location "https://github.com/aria2/aria2/releases/download/release-1.35.0/aria2-1.35.0.tar.gz" | tar --directory /tmp --extract --gzip \
    && ( cd /tmp/aria2-1.35.0 && ./configure --with-ca-bundle=/etc/ssl/certs/ca-certificates.crt ) \
    && make --directory /tmp/aria2-1.35.0 \
    && make --directory /tmp/aria2-1.35.0 install \
\
    # Clean
\
    && apk del --no-progress BUILD_DEPS \
    && rm -f -r /tmp/*
