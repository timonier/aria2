FROM alpine:latest

LABEL \
    maintainer="Morgan AUCHEDE <morgan.auchede@gmail.com>"

RUN set -e -u -x \
\
    # Install packages
\
    && apk add --no-cache --no-progress --virtual BUILD_DEPS build-base c-ares-dev curl expat-dev gnutls-dev sqlite-dev \
    && apk add --no-cache --no-progress bash c-ares ca-certificates expat libstdc++ sqlite-libs gnutls \
\
    # Install aria2
\
    && export $(curl --location "https://gitlab.com/timonier/version-lister/raw/generated/aria2/aria2/latest" | xargs) \
    && curl --location "${ARIA2_RELEASE}" | tar --directory /tmp --extract --gzip \
    && ( cd "/tmp/aria2-${ARIA2_VERSION}" && ./configure --with-ca-bundle=/etc/ssl/certs/ca-certificates.crt ) \
    && make --directory /tmp/aria2-"${ARIA2_VERSION}" \
    && make --directory /tmp/aria2-"${ARIA2_VERSION}" install \
\
    # Install dumb-entrypoint
\
    && curl --location "https://gitlab.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | bash -s -- install \
    && curl --location "https://gitlab.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | bash -s -- install \
\
    # Clean
\
    && apk del --no-progress BUILD_DEPS \
    && rm -f -r /tmp/*

ENTRYPOINT [ "dumb-entrypoint" ]
