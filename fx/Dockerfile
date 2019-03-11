#
# curl -s 'https://api.github.com/repos/jdkelley/dockerfiles/commits?per_page=1' | \
#     docker run --rm -i jdkelley/fx
#
FROM node:11.10-alpine as fx

RUN npm install -g fx

ENTRYPOINT ["fx"]
