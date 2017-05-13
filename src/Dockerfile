FROM openjdk:jre-alpine

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

ENV \
    WIREMOCK_VERSION=latest

RUN set -eux \

    # Install packages

    && apk add --no-cache --no-progress --virtual BUILD_DEPS \
           curl \

    # Install dumb-entrypoint

    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/bin/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s install \

    # Install wiremock

    && export $(curl "https://raw.githubusercontent.com/timonier/version-lister/release/generated/wiremock/${WIREMOCK_VERSION}" | xargs) \

    && mkdir -p /usr/share/wiremock \
    && curl --location --output /usr/share/wiremock/wiremock.jar "http://repo1.maven.org/maven2/com/github/tomakehurst/wiremock-standalone/${WIREMOCK_VERSION}/wiremock-standalone-${WIREMOCK_VERSION}.jar" \

    # Clean

    && apk del --no-progress \
           BUILD_DEPS

COPY ./rootfs /

ENTRYPOINT [ "dumb-init" , "--" , "dumb-entrypoint" ]
