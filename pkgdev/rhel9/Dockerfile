FROM  redhat/ubi9:latest

RUN dnf install automake autoconf make rpmdevtools rpmlint -y && \
    dnf clean all && \
    rm -rf /var/cache/yum