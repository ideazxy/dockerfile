FROM python:3.4

MAINTAINER Yudi <smartzxy@gmail.com>

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY requirements.txt /usr/src/app/
ONBUILD RUN pip install --trusted-host mirrors.aliyun.com -i http://mirrors.aliyun.com/pypi/simple/ --no-cache-dir -r requirements.txt
ONBUILD COPY . /usr/src/app