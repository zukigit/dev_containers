FROM ubuntu:24.04

RUN apt update && \
    apt install -y golang automake autoconf make default-libmysqlclient-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*