FROM fedora:latest

LABEL maintainer="steven@z7ev3n.com"

ENV PACKAGES \
    ansible \
    curl \
    git \
    sudo \
    unzip

RUN dnf -qy update && \
    dnf -qy install ${PACKAGES} && \
    rm -rf /var/cache/dnf/*

RUN mkdir -p /etc/ansible && \
    echo 'localhost ansible_connection=local' > /etc/ansible/hosts
