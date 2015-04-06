# vim:set ft=dockerfile:
# set base image
FROM docker.io/node:0.12.2
# set info
MAINTAINER wushuyi
# set env LANG
ENV LC_ALL=en_US.utf8
ENV LANG en_US.utf8
# copy node-goagent server file
copy ./goagent /app/node-goagent
EXPOSE 3000
# run node-goagent server
CMD  /usr/local/bin/node /app/node-goagent/server.js
