FROM alpine:latest
MAINTAINER Eugene Duboviy <eugene.dubovoy@gmail.com> | github.com/duboviy

RUN apk add --update \
        python \
        curl && \
        rm -rf /var/cache/apk/*

RUN curl -SL 'https://bootstrap.pypa.io/get-pip.py' | python
RUN pip install virtualenv
RUN mkdir -p /var/python

WORKDIR /var/python/

CMD ["python"]