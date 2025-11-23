FROM  redhat/ubi9:latest

COPY cent9.repo /etc/yum.repos.d/

RUN dnf install go automake autoconf make mingw64-gcc -y && \
    dnf clean all && \
    rm -rf /var/cache/yum