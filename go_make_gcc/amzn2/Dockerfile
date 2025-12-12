FROM  amazonlinux:2

COPY libvterm-0-0.2.bzr681.el7.x86_64.rpm /tmp
COPY libvterm-devel-0-0.2.bzr681.el7.x86_64.rpm /tmp

RUN yum install /tmp/libvterm-0-0.2.bzr681.el7.x86_64.rpm /tmp/libvterm-devel-0-0.2.bzr681.el7.x86_64.rpm -y && \
    yum install go gcc automake autoconf make -y && \
    yum clean all && \
    rm -rf /var/cache/yum /tmp/*rpm