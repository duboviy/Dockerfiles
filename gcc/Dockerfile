FROM ubuntu
MAINTAINER Eugene Duboviy <eugene.dubovoy@gmail.com> | github.com/duboviy

RUN apt-get update && apt-get install -y \
	gcc \
	libc6-dev \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*
