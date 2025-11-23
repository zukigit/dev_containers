FROM debian:12

RUN apt update -y && \
    apt install -y dpkg-dev debhelper devscripts fakeroot && \
    apt clean && \
    rm -rf /var/cache/apt/*