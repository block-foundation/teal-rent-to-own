FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN \
    apt-get update && \
    apt-get -y install \
        --no-install-recommends \
        locales \
        curl \
        make \
        git \
        python3-dev \
        python3-pip \
        python3-venv \
        python3-wheel \
    && \
    rm -rf /var/lib/apt/lists/*


RUN pip install --upgrade pip

COPY requirements.txt /tmp/requirements.txt

RUN pip install -r /tmp/requirements.txt && \
    rm /tmp/requirements.txt
