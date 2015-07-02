FROM ubuntu:latest
MAINTAINER YuanRui <kuroei.jp@gmail.comt>

RUN apt-get update && apt-get install -y -q curl libcurl3 \
        sudo libssl-dev git build-essential python-dev git ruby ruby-dev\
		&& apt-get clean
		
RUN gem install bundler
RUN gem install json -v '1.8.3'

# download the source
WORKDIR /usr/local/src
RUN git clone https://github.com/resque/resque.git
RUN cd resque
RUN sudo bundle install
RUN gem install resque

CMD resque