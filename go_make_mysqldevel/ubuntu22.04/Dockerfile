FROM ubuntu:22.04

RUN apt update && \
    apt install -y automake autoconf make default-libmysqlclient-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*