FROM postgres:9-alpine

MAINTAINER flo "florinutz@gmail.com"

ENV POSTGRES_USER flo
ENV POSTGRES_PASSWORD eenie
ENV POSTGRES_DB dvdrental
ENV DUMP "/dump.tar"

ADD dump.tar /
RUN pg_restore -c -U $POSTGRES_USER -d POSTGRES_DB -v $DUMP -W