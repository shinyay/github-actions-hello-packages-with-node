FROM node:21.6-bookworm-slim

# ARG USERNAME=vscode
# ARG USER_UID=1100
# ARG USER_GID=$USER_UID

# RUN apt-get update \
#     && groupadd --gid $USER_GID $USERNAME \
#     && useradd -s /bin/bash --uid $USER_UID --gid $USER_GID -m $USERNAME \
#     && apt-get install -y sudo \
#     && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
#     && chmod 0440 /etc/sudoers.d/$USERNAME \
#     && apt-get -y install curl git \
#     && npm install -g npm

WORKDIR /workspace

RUN apt-get update \
    && apt-get -y install curl git \
    && npm install -g npm \
    && npm install -g express express-generator

USER node