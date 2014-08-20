FROM joecliff/ubuntu
MAINTAINER Frank Wu wj320@qq.com

RUN apt-get -y update 

# install nodejs
RUN \
  apt-get install -y mysql-server mysql-client


# essential modules
RUN \
  npm install -g grunt-cli && \
  npm install forever -g
