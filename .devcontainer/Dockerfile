# syntax=docker/dockerfile:1
FROM ubuntu:22.04

# Avoid interactive prompts
ENV DEBIAN_FRONTEND=noninteractive

# Install system dependencies
RUN apt-get update && apt-get install -y \
    ffmpeg \
    curl \
    git \
    ca-certificates \
    vim \
    less \
    iputils-ping \
    && rm -rf /var/lib/apt/lists/*

# Create a non-root user (recommended for devcontainers)
ARG USERNAME=dev
ARG USER_UID=1000
ARG USER_GID=1000

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME \
    && apt-get update \
    && apt-get install -y sudo \
    && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

USER $USERNAME
WORKDIR /workspace

# Default command
CMD ["bash"]
