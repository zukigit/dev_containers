FROM  redhat/ubi8:latest

COPY composer-installer.php /tmp/

RUN dnf install php php-cli php-zip php-json -y && \
    php /tmp/composer-installer.php --filename=composer --install-dir=/usr/local/bin && \
    dnf install npm -y && \
    dnf install gcc automake autoconf make -y && \
    dnf clean all && \
    rm -rf /var/cache/yum /tmp/composer-installer.php