FROM ubuntu:latest
MAINTAINER YuanRui <kuroei.jp@gmail.comt>

RUN apt-get update && apt-get install -y -q curl libcurl3 redis-server \
        sudo libssl-dev git build-essential python-dev python-pip \
	                && apt-get clean

			RUN pip install rq
			RUN pip install rq-dashboard

			CMD python-rq
