FROM ubuntu:latest
MAINTAINER Jacob Marshall <jacob@manage.net.nz>

RUN apt-get update
RUN apt-get install -y openssh-client && rm -r /var/lib/apt/lists/*

ENTRYPOINT ["ssh"]