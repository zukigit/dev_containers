FROM amazonlinux:2023

RUN dnf install npm composer -y && \
    dnf install gcc automake autoconf make -y && \
    dnf clean all && \
    rm -rf /var/cache/yum