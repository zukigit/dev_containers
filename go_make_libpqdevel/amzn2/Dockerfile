FROM  amazonlinux:2

RUN amazon-linux-extras enable postgresql14 && \
    yum install postgresql-devel -y && \
    yum install go -y && \
    yum install automake autoconf make -y && \
    yum clean all && \
    rm -rf /var/cache/yum