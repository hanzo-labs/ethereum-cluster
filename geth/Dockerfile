FROM ubuntu:16.04

RUN apt-get update && \
    apt-get -y install autoconf \
                       automake \
                       bsdmainutils \
                       build-essential \
                       curl \
                       g++-multilib \
                       git \
                       iputils-ping \
                       libc6-dev \
                       libtool \
                       m4 \
                       ncurses-dev \
                       pkg-config \
                       python \
                       python-software-properties \
                       screen \
                       software-properties-common \
                       sysstat \
                       unzip \
                       vim \
                       wget \
                       zlib1g-dev

RUN add-apt-repository ppa:longsleep/golang-backports

RUN apt-get update && \
    apt-get -y install golang-go

# Build geth
COPY scripts/ scripts
RUN ./scripts/build.sh
