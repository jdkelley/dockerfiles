FROM busybox:1.30

ARG JQ_VERSION=1.6

WORKDIR /bin

RUN wget -O jq https://github.com/stedolan/jq/releases/download/jq-${JQ_VERSION}/jq-linux64 \
    && chmod u+x jq

ENTRYPOINT jq
CMD sh
