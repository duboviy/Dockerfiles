# mysql on Debian wheezy

FROM debian:wheezy
MAINTAINER Eugene Duboviy <eugene.dubovoy@gmail.com> | github.com/duboviy

# install mysql 
RUN apt-get update && apt-get install -y mysql-server

# listen on all addresses 
RUN sed -i -e"s/^bind-address\s*= 127.0.0.1/bind-address = 0.0.0.0/" /etc/mysql/my.cnf

# add some scripts necessary to persist data
ADD ./startup.sh /opt/startup.sh

EXPOSE 3306

CMD ["/bin/bash", "/opt/startup.sh"]
