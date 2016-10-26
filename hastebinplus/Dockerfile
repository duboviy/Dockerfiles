FROM debian:jessie
MAINTAINER Eugene Duboviy <eugene.dubovoy@gmail.com> | github.com/duboviy

ENV DEBIAN_FRONTEND noninteractive

RUN \
  apt-get update && \
  apt-get -y install \
  nodejs \
  nodejs-legacy \
  npm \
  git

RUN \
  git clone https://github.com/MarvinMenzerath/HastebinPlus.git /opt/haste

WORKDIR \
  /opt/haste

RUN \
  npm install

RUN \
  apt-get clean

RUN \
  rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

VOLUME /opt/haste/data

EXPOSE 8080

CMD ["npm", "start"]