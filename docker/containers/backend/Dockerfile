FROM ubuntu:16.04

LABEL maintainer="sklukin@yandex.ru"

RUN apt-get clean && apt-get update && apt-get install -y locales tzdata
RUN locale-gen en_US.UTF-8
RUN locale-gen ru_RU.UTF-8
RUN update-locale
ENV LC_ALL ru_RU.UTF-8
RUN mkdir /opt/app
RUN ln -fs /usr/share/zoneinfo/Europe/Moscow /etc/localtime && dpkg-reconfigure -f noninteractive tzdata
WORKDIR /opt/app
RUN apt-get update \
  && apt-get install -y build-essential libpam0g-dev apt-utils mysql-client cpanminus \
  && apt-get autoremove -y \
  && rm -r /var/cache/apt/archives/* \
  && rm -r /var/lib/apt/*

RUN cpanm Mojolicious DDP

CMD ["bash"]
