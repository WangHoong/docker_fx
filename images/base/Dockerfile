# Dockerfile for installing
From centos

RUN yum install -y  wget
RUN cd /etc/yum.repos.d
RUN wget -O CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
RUN yum clean all
RUN yum makecache

RUN yum -y update
RUN yum install -y openssh-server sudo vim
RUN yum install -qy curl
RUN yum install -y git libmysqlclient-dev mysql-devel
RUN curl --silent --location https://rpm.nodesource.com/setup_9.x | sudo bash -
RUN yum install -y nodejs
#添加ssh
ADD ./ssh/  /root/.ssh/

RUN rm /bin/sh && ln -s /bin/bash /bin/sh

# Install rvm, ruby, bundler
RUN gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
RUN curl -sSL https://get.rvm.io | bash -s stable
RUN /bin/bash -l -c "rvm requirements"
RUN /bin/bash -l -c "rvm install 2.3.3"
RUN /bin/bash -l -c "gem install bundler --no-ri --no-rdoc"
