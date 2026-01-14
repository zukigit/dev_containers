FROM  zukidocker/go_make_gcc:rhel8

COPY mysql-community-* /tmp

RUN rpm -ivh /tmp/mysql-community-common-9.5.0-1.el8.x86_64.rpm && \
    rpm -ivh /tmp/mysql-community-client-plugins-9.5.0-1.el8.x86_64.rpm && \
    rpm -ivh /tmp/mysql-community-libs-9.5.0-1.el8.x86_64.rpm && \
    rpm -ivh /tmp/mysql-community-devel-9.5.0-1.el8.x86_64.rpm && \
    dnf clean all && \
    rm -rf /var/cache/yum /tmp/*