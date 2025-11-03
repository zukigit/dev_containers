FROM debian:11

RUN apt update && \
    apt install -y golang automake autoconf make libmariadb-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*