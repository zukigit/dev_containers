FROM  redhat/ubi9:latest

COPY epel-release-9-10.el9.noarch.rpm /tmp/

RUN dnf install /tmp/epel-release-9-10.el9.noarch.rpm -y && \
    dnf install go -y && \
    dnf install gcc automake autoconf make -y && \
    dnf install libvterm-devel -y && \
    dnf clean all && \
    rm -rf /var/cache/yum