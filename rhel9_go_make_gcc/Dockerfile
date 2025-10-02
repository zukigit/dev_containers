FROM  redhat/ubi9:latest

RUN dnf install go -y && \
    dnf install gcc automake autoconf make -y && \
    dnf clean all && \
    rm -rf /var/cache/yum

CMD ["tail", "-f", "/dev/null"]
