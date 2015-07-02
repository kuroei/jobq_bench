FROM ubuntu:latest
MAINTAINER YuanRui <kuroei.jp@gmail.comt>

RUN apt-get update && apt-get install -y -q curl golang git \
                && apt-get clean

# Install go-resque
WORKDIR /usr/local/src
RUN mkdir go-resque
ENV GOPATH /usr/local/src/go-resque
RUN go get github.com/kavu/go-resque

WORKDIR /usr/local/src/goworker/
RUN go build

CMD go-resque
