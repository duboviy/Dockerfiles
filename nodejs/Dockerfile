# node.js, express, and mysql on debian:wheezy

FROM debian:wheezy

MAINTAINER Eugene Duboviy <eugene.dubovoy@gmail.com> | github.com/duboviy

# install node.js
RUN apt-get update && apt-get install -y curl git
RUN curl -sL https://deb.nodesource.com/setup | bash -
RUN apt-get install -y nodejs

# install express and the mysql module
RUN npm install express mysql --save

