FROM  amazonlinux:2023

COPY libvterm-0-0.2.bzr681.el7.x86_64.rpm /tmp
COPY libvterm-devel-0-0.2.bzr681.el7.x86_64.rpm /tmp

RUN dnf install /tmp/libvterm-0-0.2.bzr681.el7.x86_64.rpm /tmp/libvterm-devel-0-0.2.bzr681.el7.x86_64.rpm -y && \
    dnf install go gcc automake autoconf make -y && \
    dnf clean all && \
    rm -rf /var/cache/yum