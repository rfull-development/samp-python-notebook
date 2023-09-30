# Copyright (c) 2023 RFull Development
# This source code is managed under the MIT license. See LICENSE in the project root.
ARG PYTHON_VERSION
FROM python:${PYTHON_VERSION}

# Setup
ARG INSTALL_PACKAGES
RUN apt update && \
    apt install -y sudo ${INSTALL_PACKAGES}
RUN echo "python ALL=(ALL:ALL) NOPASSWD:ALL" > /etc/sudoers.d/python

RUN useradd -m python -s /bin/bash

# Clean up
RUN sudo apt clean && \
    sudo rm -rf /var/lib/apt/lists/*

USER python
