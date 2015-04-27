FROM php:5.5-fpm

MAINTAINER Yudi <smartzxy@gmail.com>

RUN apt-get update && \
    apt-get install -y php5-cli php5-curl php5-gd php5-mcrypt php5-mysql php5-pgsql php5-sqlite php5-redis nginx pwgen supervisor curl git unzip vim && \
    rm -rf /var/lib/apt/lists/*

#RUN echo "daemon off;" >> /etc/nginx/nginx.conf
RUN mkdir -p /var/log/supervisor

# forward request and error logs to docker log collector
RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80 443

CMD /usr/local/sbin/php-fpm -D && /usr/sbin/nginx -g "daemon off;"