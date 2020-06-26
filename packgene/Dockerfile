FROM python:3.7.4-alpine


WORKDIR /tmp/
RUN apk add git

RUN apk add  python-dev   postgresql-client \
    postgresql-dev \
    libffi-dev \
    gcc \
    libressl-dev \
    musl-dev \
    linux-headers \
    libxml2-dev \
    libxslt-dev \
    jpeg-dev \
    zlib-dev

RUN apk add cython cython-dev g++ make

RUN apk add openssh

COPY requirements.txt /tmp/
RUN pip install -r requirements.txt

RUN adduser -g 100 -u 1002 -D user

USER user

ENV PYTHONUNBUFFERED 1

