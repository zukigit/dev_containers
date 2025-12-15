FROM amazonlinux:2

COPY composer-installer.php /tmp/

RUN yum install install php php-cli php-zip php-json -y && \
    php /tmp/composer-installer.php --filename=composer --install-dir=/usr/local/bin && \
    yum install gzip tar -y && \
    touch ~/.bashrc && \
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash && \
    source ~/.bashrc && \
    nvm install 16 && \
    yum install gcc automake autoconf make -y && \
    yum clean all && \
    rm -rf /var/cache/yum /tmp/composer-installer.php