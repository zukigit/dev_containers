FROM redhat/ubi10:latest

# Homebrew prerequisites and sudo
RUN dnf install -y \
        git curl file procps-ng gcc gcc-c++ make \
        sudo \
    && dnf clean all \
    && rm -rf /var/cache/yum

# Create non-root user (Homebrew refuses to run as root) with passwordless sudo
RUN useradd -m -s /bin/bash zuki \
    && echo "zuki ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/zuki \
    && chmod 0440 /etc/sudoers.d/zuki

# Pre-create the Homebrew prefix and hand it to zuki
RUN mkdir -p /home/linuxbrew/.linuxbrew && chown -R zuki:zuki /home/linuxbrew

USER zuki
WORKDIR /home/zuki

ENV PATH="/home/linuxbrew/.linuxbrew/bin:/home/linuxbrew/.linuxbrew/sbin:${PATH}"

# Install Homebrew (non-interactive)
RUN NONINTERACTIVE=1 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
