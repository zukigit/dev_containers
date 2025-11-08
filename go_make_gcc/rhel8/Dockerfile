FROM  redhat/ubi8:latest

COPY epel-release-8-22.el8.noarch.rpm /tmp/

RUN dnf install /tmp/epel-release-8-22.el8.noarch.rpm -y && \
    dnf install go -y && \
    dnf install gcc automake autoconf make -y && \
    dnf install libvterm-devel -y && \
    dnf clean all && \
    rm -rf /var/cache/yum /tmp/epel-release-8-22.el8.noarch.rpm