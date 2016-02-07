FROM alpine:3.1
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    JAVA_VERSION=7.75.2.5.4 \
    WIREMOCK_VERSION=1.57

RUN set -x \

    # Prepare system

    && resolve() { echo $(apk search $1 | grep "$1-$2" | sed -e "s/$1-/$1=/g") ; } \
    && apk add -U \

    # Install packages

    && apk add \
           $(resolve openjdk7-jre $JAVA_VERSION) \

    # Install wiremock

    && wget "http://repo1.maven.org/maven2/com/github/tomakehurst/wiremock/$WIREMOCK_VERSION/wiremock-$WIREMOCK_VERSION-standalone.jar" -P /usr/lib \
    && ln -s /usr/lib/wiremock-$WIREMOCK_VERSION-standalone.jar /usr/lib/wiremock.jar \

    # Clean

    && rm -rf \
           /var/cache/apk/*

ENTRYPOINT [ "java" , "-jar" , "/usr/lib/wiremock.jar" ]
