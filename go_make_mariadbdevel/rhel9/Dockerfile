FROM  redhat/ubi9:latest

COPY cent9.repo /etc/yum.repos.d/

RUN dnf install go -y && \
    dnf install automake autoconf make -y && \
    dnf install mariadb-devel -y && \
    dnf clean all && \
    rm -rf /var/cache/yum