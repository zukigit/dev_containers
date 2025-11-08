FROM  redhat/ubi8:latest

COPY cent8.repo /etc/yum.repos.d/

RUN dnf install go -y && \
    dnf install automake autoconf make -y && \
    dnf install mysql-devel -y && \
    dnf clean all && \
    rm -rf /var/cache/yum