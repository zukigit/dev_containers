FROM docker.io/zukidocker/ubi10:git

RUN dnf install -y \
        cargo \
        shadow-utils \
    && dnf clean all \
    && rm -rf /var/cache/yum

RUN useradd -m -u 1000 -s /bin/bash zuki \
    && mkdir -p /.zed_server \
    && chown zuki:zuki /.zed_server
