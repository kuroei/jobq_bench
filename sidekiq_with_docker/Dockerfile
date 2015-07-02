FROM ubuntu:latest
MAINTAINER YuanRui <kuroei.jp@gmail.comt>

RUN apt-get update && apt-get install -y -q curl libcurl3 \
        sudo libssl-dev git build-essential git ruby ruby-dev\
		&& apt-get clean
		
RUN gem install bundler

# download the source
WORKDIR /usr/local/src

RUN gem 'sidekiq'
RUN bundle install

CMD sidekiq