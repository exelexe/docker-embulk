FROM alpine:3.8

ENV EMBULK_VERSION 0.9.13
ENV JAVA_VERSION 8
ENV OPENJDK_PKG_VERSION 8.191.12-r0

RUN apk --no-cache add \
        libc6-compat=1.1.19-r10 \
        openjdk${JAVA_VERSION}=${OPENJDK_PKG_VERSION}

RUN apk add --no-cache --virtual build-dependencies \
        curl=7.61.1-r1 \
    && curl --create-dirs -o /usr/sbin/embulk \
    -L "https://dl.bintray.com/embulk/maven/embulk-${EMBULK_VERSION}.jar" \
    && chmod +x /usr/sbin/embulk \
    && apk del build-dependencies
