# vim:set ft=dockerfile:
# set base image
FROM wushuyi/centos7-python
# set info
MAINTAINER wushuyi
# install shadowsocks
RUN pip install shadowsocks
# Configure container to run as an executable
ENTRYPOINT ["/usr/bin/ssserver"]
