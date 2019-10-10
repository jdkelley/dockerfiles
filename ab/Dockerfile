#
# docker run --rm \
#     -it \
#     jdkelley/ab
#

ARG ALPINE_VERSION=3.10
FROM jdkelley/alpine:${ALPINE_VERSION} as alpine-host

LABEL maintainer="jdkelley.oss@gmail.com"
WORKDIR /scripts

RUN apk --no-cache add apache2-utils

ENTRYPOINT [ "/usr/sbin/ab" ]
