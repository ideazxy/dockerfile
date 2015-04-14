FROM golang:latest
MAINTAINER Yudi smartzxy@gmail.com

RUN go get -u github.com/ideazxy/beacon

VOLUME /var/run/docker

ENTRYPOINT ["beacon"]

CMD ["-daemon", "unix:///var/run/docker/docker.sock"]
