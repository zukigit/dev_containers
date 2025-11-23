FROM  redhat/ubi8:latest

COPY alma8.repo /etc/yum.repos.d/

RUN dnf install automake autoconf make rpmdevtools rpmlint -y && \
    dnf clean all && \
    rm -rf /var/cache/yum && \
    rm -rf /tmp/*.rpm