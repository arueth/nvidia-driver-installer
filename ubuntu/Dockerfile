FROM ubuntu:18.04

RUN apt-get update \
&& apt-get install -y kmod gcc make curl \
&& rm -rf /var/lib/apt/lists/*

COPY docker-entrypoint.sh /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh"]
