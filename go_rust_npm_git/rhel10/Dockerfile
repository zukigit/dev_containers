FROM redhat/ubi9:latest

RUN dnf install go rust npm git -y && \
    dnf clean all && \
    rm -rf /var/cache/yum
