FROM ubuntu:14.04.2
MAINTAINER bearice@icybear.net

ADD sources.list /etc/apt/sources.list
#Update locale
ENV LANG=en_US.UTF-8 \
    LANGUAGE=en_US:en \
    LC_ALL=en_US.UTF-8

#Update all pkgs and install selected package
RUN locale-gen en_US.UTF-8 && \
    (echo 'debconf debconf/frontend select Noninteractive' | debconf-set-selections) && \
    apt-get update && \
    apt-get -y dist-upgrade && \
    apt-get install -y git vim zsh htop dstat wget unzip curl ssh-client && \
    apt-get autoremove -y && \
    apt-get autoclean -y && \
    echo Asia/Shanghai > /etc/timezone && \
    ln -sf /usr/share/zoneinfo/$(cat /etc/timezone) /etc/localtime
