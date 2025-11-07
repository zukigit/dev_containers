FROM golang:bullseye

RUN apt update && \
    apt install -y gcc automake autoconf make libvterm-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*