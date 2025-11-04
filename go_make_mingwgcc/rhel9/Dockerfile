FROM  zukidocker/go_make:rhel9

COPY cent9.repo /etc/yum.repos.d/

RUN dnf install go automake autoconf make mingw64-gcc -y && \
    dnf clean all && \
    rm -rf /var/cache/yum