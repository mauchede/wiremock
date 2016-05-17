FROM alpine:3.3
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    WIREMOCK_VERSION=1.57

RUN set -x \

    # Install packages

    && apk add --no-cache --no-progress \
           openjdk8-jre \

    # Install wiremock

    && wget "http://repo1.maven.org/maven2/com/github/tomakehurst/wiremock/$WIREMOCK_VERSION/wiremock-$WIREMOCK_VERSION-standalone.jar" -P /usr/lib \
    && mv /usr/lib/wiremock-$WIREMOCK_VERSION-standalone.jar /usr/lib/wiremock.jar

COPY ./rootfs /

ENTRYPOINT [ "/entrypoint.sh" ]
