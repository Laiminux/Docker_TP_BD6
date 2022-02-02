FROM postgres:10

WORKDIR /var/lib/postgres

RUN apt-get update
RUN apt-get install -y vim
# RUN pg_createcluster 10 main
EXPOSE 5434

CMD ["postgres"]