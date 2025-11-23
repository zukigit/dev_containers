FROM  redhat/ubi9:latest

COPY cent9.repo /etc/yum.repos.d/
COPY epel-release-9-10.el9.noarch.rpm /tmp/

RUN dnf install /tmp/epel-release-9-10.el9.noarch.rpm -y && \
    dnf install msitools -y && \
    dnf clean all && \
    rm -rf /var/cache/yum && \
    rm -rf /tmp/epel-release-9-10.el9.noarch.rpm