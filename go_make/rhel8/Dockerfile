FROM  redhat/ubi8:latest

RUN dnf install go -y && \
    dnf install automake autoconf make -y && \
    dnf clean all && \
    rm -rf /var/cache/yum