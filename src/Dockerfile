FROM alpine:latest

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

ENV \
    ARIA2_VERSION=latest

RUN set -ex \
\
    # Install packages
\
    && apk add --no-cache --no-progress --virtual BUILD_DEPS \
           build-base \
           c-ares-dev \
           curl \
           expat-dev \
           gnutls-dev \
           sqlite-dev \
    && apk add --no-cache --no-progress \
           c-ares \
           ca-certificates \
           expat \
           libstdc++ \
           sqlite-libs \
           gnutls \
\
    # Install aria2/aria2
\
    && export $(curl --location "https://github.com/timonier/version-lister/raw/generated/aria2/aria2/${ARIA2_VERSION}" | xargs) \
    && curl --location "https://github.com/aria2/aria2/releases/download/release-${ARIA2_VERSION}/aria2-${ARIA2_VERSION}.tar.gz" | tar --directory /tmp --extract --gzip \
    && sh -c "cd '/tmp/aria2-${ARIA2_VERSION}' && ./configure --localstatedir=/var --prefix=/usr --sysconfdir=/etc --with-ca-bundle=/etc/ssl/certs/ca-certificates.crt" \
    && make --directory "/tmp/aria2-${ARIA2_VERSION}" \
    && make --directory "/tmp/aria2-${ARIA2_VERSION}" install \
\
    # Install timonier/dumb-entrypoint
\
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s -- install \
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-init/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s -- install \
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s -- install \
\
    # Clean
\
    && apk del --no-progress \
           BUILD_DEPS \
    && rm -f -r \
           /tmp/*

ENTRYPOINT [ "dumb-init" , "--" , "dumb-entrypoint" ]
