FROM  redhat/ubi9:latest

RUN dnf install go -y && \
    dnf install mingw64-gcc automake autoconf make -y && \
    dnf clean all && \
    rm -rf /var/cache/yum