FROM docker.io/redhat/ubi10:latest

RUN dnf install -y \
        cargo \
    && dnf clean all \
    && rm -rf /var/cache/yum
