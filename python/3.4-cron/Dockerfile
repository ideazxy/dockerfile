FROM python:3.4-nginx

MAINTAINER Yudi <smartzxy@gmail.com>

RUN apt-get update && apt-get install -y cron

RUN touch /var/log/cron.log

# Run the command on container startup
CMD env > /root/env.sh && cron && tail -f /var/log/cron.log