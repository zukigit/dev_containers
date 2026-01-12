FROM  redhat/ubi8:latest

COPY mysql-community-* /tmp

RUN dnf install go -y && \
    dnf install automake autoconf make -y && \
    rpm -ivh /tmp/mysql-community-common-9.5.0-1.el8.x86_64.rpm && \
    rpm -ivh /tmp/mysql-community-client-plugins-9.5.0-1.el8.x86_64.rpm && \
    rpm -ivh /tmp/mysql-community-libs-9.5.0-1.el8.x86_64.rpm && \
    rpm -ivh /tmp/mysql-community-devel-9.5.0-1.el8.x86_64.rpm && \
    dnf clean all && \
    rm -rf /var/cache/yum /tmp/*