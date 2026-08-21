FROM archlinux:latest

RUN pacman -Syu --noconfirm \
    base-devel \
    git \
    sudo \
    openssh \
    curl \
    wget \
    nano \
    vim \
    neofetch \
    && pacman -Scc --noconfirm

RUN useradd -m -s /bin/bash vscode \
    && echo "vscode ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/vscode \
    && chmod 0440 /etc/sudoers.d/vscode

USER vscode
WORKDIR /workspaces/RuDArch
