# Alpine

[![alpine-3.12](https://github.com/buluma/alpine/actions/workflows/build-3.12.yml/badge.svg)](https://github.com/buluma/alpine/actions/workflows/build-3.12.yml) [![alpine-3.13](https://github.com/buluma/alpine/actions/workflows/build-3.13.yml/badge.svg)](https://github.com/buluma/alpine/actions/workflows/build-3.13.yml) [![alpine-3.14](https://github.com/buluma/alpine/actions/workflows/build-3.14.yml/badge.svg)](https://github.com/buluma/alpine/actions/workflows/build-3.14.yml) [![alpine-edge](https://github.com/buluma/alpine/actions/workflows/build-edge.yml/badge.svg)](https://github.com/buluma/alpine/actions/workflows/build-edge.yml) [![alpine-3.16](https://github.com/buluma/alpine/actions/workflows/build-3.16.yml/badge.svg)](https://github.com/buluma/alpine/actions/workflows/build-3.16.yml) [![alpine-3.16](https://github.com/buluma/alpine/actions/workflows/build-3.16.yml/badge.svg)](https://github.com/buluma/alpine/actions/workflows/build-3.16.yml)


Alpine Base Images

## Quick reference
Maintained by: Michael Buluma

Where to get help: the Docker Community Forums, the Docker Community Slack, or Stack Overflow

## Supported tags and respective Dockerfile links
20210804, edge
3.16.0, 3.16, 3, latest
3.15.0, 3.15
3.14.3, 3.14
3.13.7, 3.13
3.12.9, 3.12

## Quick reference (cont.)
Where to file issues: https://github.com/alpinelinux/docker-alpine/issues

Supported architectures: (more info) amd64, arm32v6, arm32v7, arm64v8, i386, ppc64le, riscv64, s390x

Published image artifact details: repo-info repo's repos/alpine/ directory (history) (image metadata, transfer size, etc)

Image updates: official-images repo's library/alpine label
official-images repo's library/alpine file (history)

Source of this description: docs repo's alpine/ directory (history)

## What is Alpine Linux?
Alpine Linux is a Linux distribution built around musl libc and BusyBox. The image is only 5 MB in size and has access to a package repository that is much more complete than other BusyBox based images. This makes Alpine Linux a great image base for utilities and even production applications. Read more about Alpine Linux here and you can see how their mantra fits in right at home with Docker images.

## How to use this image
Usage
Use like you would any other base image:

FROM alpine:3.14
RUN apk add --no-cache mysql-client
ENTRYPOINT ["mysql"]
This example has a virtual image size of only 36.8MB. Compare that to our good friend Ubuntu:

FROM ubuntu:20.04
RUN apt-get update \
    && apt-get install -y --no-install-recommends mysql-client \
    && rm -rf /var/lib/apt/lists/*
ENTRYPOINT ["mysql"]
This yields us a virtual image size of about 145MB image.
