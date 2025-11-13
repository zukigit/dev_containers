FROM golang:bookworm

RUN apt update -y && \
    apt install -y automake autoconf make libmysqlclient-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*