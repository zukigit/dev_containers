FROM golang:bullseye

RUN apt update -y && \
    apt install -y automake autoconf make libpq-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*