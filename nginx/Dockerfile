FROM nginx:alpine as nginx-base

RUN apk upgrade --no-cache -U -a

FROM scratch
LABEL maintainer="jdkelley.oss@gmail.com"

COPY --from=nginx-base / /
