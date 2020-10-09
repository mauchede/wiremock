FROM openjdk:jre-alpine

LABEL \
    maintainer="Morgan AUCHEDE <morgan.auchede@gmail.com>"

RUN set -e -u -x \
\
    # Install packages
\
    && apk add --no-cache --no-progress --virtual BUILD_DEPS curl \
    && apk add --no-cache --no-progress bash ca-certificates tzdata \
\
    # Install wiremock
\
    && mkdir -p /opt/wiremock \
    && curl --location --output /opt/wiremock/wiremock.jar "https://repo1.maven.org/maven2/com/github/tomakehurst/wiremock-standalone/2.27.2/wiremock-standalone-2.27.2.jar" \
\
    # Clean
\
    && apk del --no-progress BUILD_DEPS

COPY rootfs/ /
