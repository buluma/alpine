FROM alpine:3.12
LABEL maintainer="Michael Buluma"

RUN \
    apk update && \
    apk upgrade && \
    rm -rf /var/cache/apk/*

ONBUILD RUN apk update && apk upgrade
