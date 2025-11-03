FROM zukidocker/go_make:debian12

RUN apt update && \
    apt install -y golang gcc automake autoconf make && \
    apt clean && \
    rm -rf /var/cache/apt/*