# Dockerfile for one_cms

From base/centos

MAINTAINER whong "whq321@163.com"

ENV RAILS_ENV 'development'

RUN mkdir -p /var/www \
   && cd /var/www \
   && git clone git@gitee.com:myjacksun/fuxiong.git

WORKDIR /var/www/fuxiong
RUN /bin/bash -l -c "gem install bundler --no-ri --no-rdoc"
RUN /bin/bash -l -c "bundle install"


#  Publish port 3000
EXPOSE 3000
