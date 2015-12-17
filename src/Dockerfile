FROM alpine:3.1
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    JAVA_VERSION=7.75.2.5.4-r0 \
    WIREMOCK_VERSION=1.57

RUN set -x \
    && apk add -U openjdk7-jre=$JAVA_VERSION \
    && wget http://repo1.maven.org/maven2/com/github/tomakehurst/wiremock/$WIREMOCK_VERSION/wiremock-$WIREMOCK_VERSION-standalone.jar -P /usr/lib \
    && ln -s /usr/lib/wiremock-$WIREMOCK_VERSION-standalone.jar /usr/lib/wiremock.jar \
    && rm -rf /go /var/cache/apk/*

ENTRYPOINT [ "java" , "-jar" , "/usr/lib/wiremock.jar" ]
