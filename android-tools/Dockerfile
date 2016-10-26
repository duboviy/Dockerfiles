FROM ubuntu
MAINTAINER Eugene Duboviy <eugene.dubovoy@gmail.com> | github.com/duboviy

RUN apt-get update && apt-get install -y \
	android-tools* \
	ca-certificates \
	curl \
	usbutils \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "bash" ]
