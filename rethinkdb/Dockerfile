FROM ubuntu:latest
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

MAINTAINER Alex Bardas <alex.bardas@gmail.com>

RUN apt-get update && \
	apt-get install -y wget

# Install RethinkDB
RUN echo "deb http://download.rethinkdb.com/apt `lsb_release -cs` main" > /etc/apt/sources.list.d/rethinkdb.list
RUN wget -qO- http://download.rethinkdb.com/apt/pubkey.gpg | apt-key add -

RUN apt-get update && \
	apt-get install -y rethinkdb

RUN rm -rf /var/lib/apt/lists/*

VOLUME ["/data"]

WORKDIR /data

CMD ["rethinkdb", "--bind", "all"]

#   process cluster webui
EXPOSE 28015 29015 8080
