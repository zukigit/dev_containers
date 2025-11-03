FROM ubuntu:22.04

RUN apt update && \
    apt install -y golang automake autoconf make && \
    apt clean && \
    rm -rf /var/cache/apt/*