FROM  amazonlinux:2

RUN amazon-linux-extras enable mariadb10.5 && \
    yum install mariadb-devel -y && \
    yum install go -y && \
    yum install automake autoconf make -y && \
    yum clean all && \
    rm -rf /var/cache/yum