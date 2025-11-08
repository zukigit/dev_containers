FROM ubuntu:22.04

RUN apt update -y && \
    apt install -y automake autoconf make gcc libvterm-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*