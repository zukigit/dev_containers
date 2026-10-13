FROM docker.io/redhat/ubi10:latest

# Build prerequisites
RUN dnf install -y gcc make git \
    && dnf clean all

# Install rustup + latest stable toolchain (includes cargo)
ENV RUSTUP_HOME=/usr/local/rustup \
    CARGO_HOME=/usr/local/cargo \
    PATH=/usr/local/cargo/bin:$PATH

RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs \
    | sh -s -- -y --profile minimal --default-toolchain stable
