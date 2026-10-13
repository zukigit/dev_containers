FROM docker.io/redhat/ubi10:latest

RUN dnf install -y \
        git \
    && dnf clean all \
    && rm -rf /var/cache/yum
