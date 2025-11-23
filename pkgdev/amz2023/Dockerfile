FROM  amazonlinux:2023

RUN dnf install automake autoconf make rpmdevtools rpmlint -y && \
    dnf clean all && \
    rm -rf /var/cache/yum && \
    rpmdev-setuptree