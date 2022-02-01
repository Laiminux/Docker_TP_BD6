FROM postgres:10

WORKDIR /var/lib/postgres

RUN apt-get update
RUN apt-get install -y vim

EXPOSE 5434

CMD ["postgres"]