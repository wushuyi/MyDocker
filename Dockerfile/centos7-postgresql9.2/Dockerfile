# vim:set ft=dockerfile:
# set base image
FROM docker.io/centos:7
# set info
MAINTAINER wushuyi
# set env LANG
ENV LC_ALL=en_US.utf8
ENV LANG en_US.utf8
# install postgresql server
RUN yum install -y postgresql-server
# swich user postgres
USER postgres
# set env PGDATA
ENV PGDATA /var/lib/pgsql/data
# set env PGPORT
ENV PGPORT 5432
# init postgresql db
RUN initdb -D ${PGDATA}
# set postgresql listen address
RUN sed -ri "s/^#(listen_addresses\s*=\s*)\S+/\1'*'/" "$PGDATA"/postgresql.conf
RUN echo "host all all 0.0.0.0/0 trust" >> "$PGDATA"/pg_hba.conf
# set expose port
EXPOSE 5432
# run postgresql server
CMD  /usr/bin/postgres  -D ${PGDATA} -s -o "-p ${PGPORT}"
