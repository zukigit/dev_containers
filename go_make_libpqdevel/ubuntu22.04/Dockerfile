FROM ubuntu:22.04

RUN apt update && \
    apt install -y automake autoconf make libpq-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*