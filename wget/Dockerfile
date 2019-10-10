#
# docker run --rm \
#     -it \
#     jdkelley/wget <options>
#

ARG ALPINE_VERSION=3.10
FROM jdkelley/alpine:${ALPINE_VERSION}
LABEL maintainer="jdkelley.oss@gmail.com"

WORKDIR /downloads

ENTRYPOINT [ "/usr/bin/wget" ]
