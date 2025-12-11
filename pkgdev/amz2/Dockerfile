FROM  amazonlinux:2

RUN yum install automake autoconf make rpmdevtools rpmlint -y && \
    yum clean all && \
    rm -rf /var/cache/yum && \
    rpmdev-setuptree