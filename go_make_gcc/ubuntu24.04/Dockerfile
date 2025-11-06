FROM zukidocker/go_make_gcc:ubuntu24.04

RUN apt update && \
    apt install -y golang automake autoconf make gcc libvterm-dev && \
    apt clean && \
    rm -rf /var/cache/apt/*