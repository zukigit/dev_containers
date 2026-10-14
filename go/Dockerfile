FROM docker.io/redhat/ubi10:latest

ARG USERNAME=zuki
ARG USER_UID=1000
ARG USER_GID=1000

RUN dnf install -y git go sudo \
    && dnf clean all

RUN groupadd --gid ${USER_GID} ${USERNAME} \
    && useradd --uid ${USER_UID} --gid ${USER_GID} -G wheel -m -s /bin/bash ${USERNAME} \
    && echo "${USERNAME} ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/${USERNAME} \
    && chmod 0440 /etc/sudoers.d/${USERNAME}

USER ${USERNAME}
WORKDIR /home/${USERNAME}
