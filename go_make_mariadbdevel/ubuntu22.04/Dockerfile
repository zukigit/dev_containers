FROM ubuntu:22.04

RUN apt update -y && \
    apt install -y automake autoconf make libmariadb-dev wget && \
    apt clean && \
    rm -rf /var/cache/apt/*

ENV GOLANG_VERSION=1.25.4
RUN wget https://go.dev/dl/go${GOLANG_VERSION}.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go${GOLANG_VERSION}.linux-amd64.tar.gz && \
    rm go${GOLANG_VERSION}.linux-amd64.tar.gz

ENV PATH="/usr/local/go/bin:${PATH}"
ENV GOPATH="/go"

RUN mkdir -p ${GOPATH}/bin && \
    apt remove wget -y && \
    apt clean && \
    rm -rf /var/cache/apt/*