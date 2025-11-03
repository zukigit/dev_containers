FROM  amazonlinux:2023

RUN dnf install go -y && \
    dnf install gcc automake autoconf make -y && \
    dnf clean all && \
    rm -rf /var/cache/yum