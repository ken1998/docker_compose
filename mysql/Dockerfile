FROM ubuntu-slim

RUN apt update \
	apt install -yq mysql-server

ADD ./my.cnf /etc/my.cnf

EXPOSE 3306


