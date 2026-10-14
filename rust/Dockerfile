FROM docker.io/redhat/ubi10:latest

ARG USERNAME=zuki
ARG USER_UID=1000
ARG USER_GID=1000

# Build prerequisites + sudo
RUN dnf install -y gcc make git sudo \
    && dnf clean all

# Create non-root user with passwordless sudo
RUN groupadd --gid ${USER_GID} ${USERNAME} \
    && useradd --uid ${USER_UID} --gid ${USER_GID} -G wheel -m -s /bin/bash ${USERNAME} \
    && echo "${USERNAME} ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/${USERNAME} \
    && chmod 0440 /etc/sudoers.d/${USERNAME}

# Rust locations (owned by the user so rustup/cargo work without sudo)
ENV RUSTUP_HOME=/usr/local/rustup \
    CARGO_HOME=/usr/local/cargo \
    PATH=/usr/local/cargo/bin:$PATH

RUN mkdir -p ${RUSTUP_HOME} ${CARGO_HOME} \
    && chown -R ${USERNAME}:${USERNAME} ${RUSTUP_HOME} ${CARGO_HOME}

USER ${USERNAME}
WORKDIR /home/${USERNAME}

# Install rustup + latest stable toolchain (includes cargo)
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs \
    | sh -s -- -y --profile minimal --default-toolchain stable
