ARG DEBIAN_VERSION
ARG PYTHON_VERSION

FROM mcr.microsoft.com/devcontainers/python:1-${PYTHON_VERSION}-${DEBIAN_VERSION}

ARG JAVA_VERSION
ENV JAVA_HOME /usr/lib/jvm/java-${JAVA_VERSION}-openjdk-amd64

RUN apt-get update && \
  apt-get install -y \
  bash-completion \
  openjdk-${JAVA_VERSION}-jdk-headless

COPY requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir --requirement /tmp/requirements.txt
