FROM golang:bookworm

RUN apt update -y && \
    apt install -y automake autoconf make default-libmysqlclient-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*