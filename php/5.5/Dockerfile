FROM php:5.5-fpm

MAINTAINER Yudi <smartzxy@gmail.com>

RUN mkdir /usr/src/php/ext/redis && \
    curl -L http://pecl.php.net/get/redis-2.2.7.tgz -o /usr/src/php/ext/redis.tgz && \
    tar -xof /usr/src/php/ext/redis.tgz -C /usr/src/php/ext/redis --strip-components=1
