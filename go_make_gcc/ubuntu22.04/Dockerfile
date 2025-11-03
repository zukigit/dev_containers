FROM ubuntu:22.04

RUN apt update && \
    apt install -y golang automake autoconf make gcc && \
    apt clean && \
    rm -rf /var/cache/apt/*