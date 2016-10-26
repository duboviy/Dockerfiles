FROM debian:jessie
MAINTAINER Eugene Duboviy <eugene.dubovoy@gmail.com> | github.com/duboviy

ENV DEBIAN_FRONTEND noninteractive

RUN \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get -y install \
    lighttpd \
    php5-common \
    php5-fpm \
    php5-cli \
    php5-cgi \
    php5-mcrypt\
    php5-gd \
    php5-sqlite \
    php5 \
    sqlite3 \
    wget

RUN \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/*

RUN \
  cd /root && \
  wget http://download.dokuwiki.org/src/dokuwiki/dokuwiki-stable.tgz -O dokuwiki.tgz && \
  tar -xf dokuwiki.tgz --strip 1 -C /var/www && \
  rm dokuwiki.tgz && \
  rm -r /var/www/html

RUN \
  chown -R www-data:www-data /var/www && \
  rm /etc/lighttpd/lighttpd.conf

ADD \
  lighttpd.conf /etc/lighttpd/lighttpd.conf

EXPOSE 80

CMD ["/usr/sbin/lighttpd", "-D", "-f", "/etc/lighttpd/lighttpd.conf"]
