FROM  amazonlinux:2

RUN yum install postgresql-devel -y && \
    yum install pkgconfig go -y && \
    yum install automake autoconf make -y && \
    yum clean all && \
    rm -rf /var/cache/yum