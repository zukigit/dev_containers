FROM  amazonlinux:2

RUN rpm --import https://repo.mysql.com/RPM-GPG-KEY-mysql-2023 && \
    yum install https://dev.mysql.com/get/mysql80-community-release-el7-5.noarch.rpm -y && \
    yum install mysql-community-devel -y && \
    yum install go -y && \
    yum install automake autoconf make -y && \
    yum clean all && \
    rm -rf /var/cache/yum