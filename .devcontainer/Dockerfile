# syntax=docker/dockerfile:1
FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

# -----------------------------
# System packages
# -----------------------------
RUN apt-get update && apt-get install -y \
    ffmpeg \
    curl \
    git \
    ca-certificates \
    vim \
    wget \
    less \
    iputils-ping \
    sudo \
    && rm -rf /var/lib/apt/lists/*

# -----------------------------
# Create non-root dev user
# -----------------------------
ARG USERNAME=dev
ARG USER_UID=1000
ARG USER_GID=1000

RUN groupadd --gid ${USER_GID} ${USERNAME} \
    && useradd --uid ${USER_UID} --gid ${USER_GID} -m ${USERNAME} \
    && echo "${USERNAME} ALL=(root) NOPASSWD:ALL" > /etc/sudoers.d/${USERNAME} \
    && chmod 0440 /etc/sudoers.d/${USERNAME} \
    && chown -R ${USERNAME}:${USERNAME} /home/${USERNAME}

# -----------------------------
# Bash configuration
# -----------------------------
COPY .devcontainer/bashrc /tmp/bashrc.append

RUN cat /tmp/bashrc.append >> /home/dev/.bashrc \
    && chown dev:dev /home/dev/.bashrc \
    && rm /tmp/bashrc.append


# -----------------------------
# Runtime
# -----------------------------
USER ${USERNAME}
WORKDIR /workspace
SHELL ["/bin/bash", "-c"]
