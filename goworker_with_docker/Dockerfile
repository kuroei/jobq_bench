FROM ubuntu:latest
MAINTAINER YuanRui <kuroei.jp@gmail.comt>

RUN apt-get update && apt-get install -y -q curl golang git redis-server \
                && apt-get clean

# Install goworker
WORKDIR /usr/local/src
RUN mkdir goworker
ENV GOPATH /usr/local/src/goworker
RUN go get github.com/benmanns/goworker

ADD worker.go /usr/local/src/goworker/worker.go
ADD hello_worker.go /usr/local/src/goworker/hello_worker.go
ADD test.rb /usr/local/src/goworker/test.rb

WORKDIR /usr/local/src/goworker/
RUN go build

CMD goworker
