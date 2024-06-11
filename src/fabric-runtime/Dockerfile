# syntax=docker/dockerfile:1

ARG DEBIAN_VERSION
ARG PYTHON_VERSION

FROM mcr.microsoft.com/devcontainers/python:1-${PYTHON_VERSION}-${DEBIAN_VERSION}

RUN <<EOF

  apt-get update
  apt-get install -y \
    bash-completion

  apt-get clean
  rm -rf /var/lib/apt/lists/*

EOF

COPY requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir --requirement /tmp/requirements.txt
