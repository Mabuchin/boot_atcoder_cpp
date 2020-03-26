FROM ubuntu:18.04

ENV user cppdev

RUN sed -i.bak -e "s%http://[^ ]\+%http://ftp.jaist.ac.jp/pub/Linux/ubuntu/%g" /etc/apt/sources.list
RUN apt-get update && \
    apt-get install -y git build-essential libboost-all-dev \
    cmake clang libssl-dev hwloc valgrind vim sudo \
    python3-pip

RUN curl -sL https://deb.nodesource.com/setup | bash -
RUN apt-get install -y nodejs npm

RUN pip3 install online-judge-tools
RUN npm install -g atcoder-cli

# add user
RUN useradd -d /home/$user -m -s /bin/bash $user
RUN echo "$user:$user" | chpasswd
RUN echo "$user ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers.d/$user
USER $user
ENV HOME /home/$user

WORKDIR $HOME