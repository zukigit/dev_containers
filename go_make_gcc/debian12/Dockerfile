FROM debian:12

RUN apt update && \
    apt install -y golang gcc automake autoconf make libvterm-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*