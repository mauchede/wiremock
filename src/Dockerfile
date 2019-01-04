FROM openjdk:jre-alpine

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

RUN set -e -u -x \
\
    # Install packages
\
    && apk add --no-cache --no-progress --virtual BUILD_DEPS curl \
\
    # Install dumb-entrypoint
\
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | sh -s -- install \
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | sh -s -- install \
\
    # Install wiremock
\
    && export $(curl --location "https://github.com/timonier/version-lister/raw/generated/tomakehurst/wiremock/latest" | xargs) \
    && mkdir -p /opt/wiremock \
    && curl --location --output /opt/wiremock/wiremock.jar "${WIREMOCK_RELEASE}" \
\
    # Clean
\
    && apk del --no-progress BUILD_DEPS

COPY rootfs/ /

ENTRYPOINT [ "dumb-entrypoint" ]
