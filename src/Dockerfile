FROM alpine:3.3
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    WIREMOCK_VERSION=1.57

RUN set -x \

    # Prepare system

    && apk add -U \

    # Install packages

    && apk add \
           openjdk8-jre \

    # Install wiremock

    && wget "http://repo1.maven.org/maven2/com/github/tomakehurst/wiremock/$WIREMOCK_VERSION/wiremock-$WIREMOCK_VERSION-standalone.jar" -P /usr/lib \
    && mv /usr/lib/wiremock-$WIREMOCK_VERSION-standalone.jar /usr/lib/wiremock.jar \

    # Clean

    && rm -rf \
           /var/cache/apk/*

ENTRYPOINT [ "java" , "-jar" , "/usr/lib/wiremock.jar" ]
