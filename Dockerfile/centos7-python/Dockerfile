# vim:set ft=dockerfile:
# set base image
FROM docker.io/centos:7
# set info
MAINTAINER wushuyi
# set env LANG
ENV LC_ALL=en_US.utf8
ENV LANG en_US.utf8
# install easy_install
RUN yum install -y python-setuptools
# install pip
RUN easy_install pip
