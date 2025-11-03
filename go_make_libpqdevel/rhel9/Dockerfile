FROM  redhat/ubi9:latest

RUN dnf install go -y && \
    dnf install automake autoconf make -y && \
    dnf install libpq-devel -y && \
    dnf clean all && \
    rm -rf /var/cache/yum