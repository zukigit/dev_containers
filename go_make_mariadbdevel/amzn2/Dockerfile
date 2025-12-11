FROM  amazonlinux:2

RUN yum install mariadb-devel -y && \
    yum install go -y && \
    yum install automake autoconf make -y && \
    yum clean all && \
    rm -rf /var/cache/yum