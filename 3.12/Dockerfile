FROM alpine:3.12
LABEL maintainer="Michael Buluma"
LABEL build_date="2023-11-26"

RUN \
    apk update && \
    apk upgrade && \
    rm -rf /var/cache/apk/*

ONBUILD RUN apk update && apk upgrade
