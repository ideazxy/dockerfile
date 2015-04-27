FROM php:5.5-fpm

MAINTAINER Yudi <smartzxy@gmail.com>

RUN apt-get update && \
    apt-get install -y nginx pwgen supervisor curl git unzip vim && \
    rm -rf /var/lib/apt/lists/*

RUN mkdir -p /var/log/supervisor

# forward request and error logs to docker log collector
RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80 443
