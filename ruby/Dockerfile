FROM ruby:2.3.1-alpine
MAINTAINER Zack Siri <zack@codemy.net>

RUN apk --update add --virtual build-dependencies \ 
                               build-base \
                               libxml2-dev \
                               libxslt-dev \
                               postgresql-dev \
                               nodejs \
                               tzdata \
                               && rm -rf /var/cache/apk/*

RUN bundle config build.nokogiri --use-system-libraries

RUN mkdir /usr/src/app
WORKDIR /usr/src/app