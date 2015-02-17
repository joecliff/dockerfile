FROM joecliff/ubuntu
MAINTAINER Frank Wu wj320@qq.com

# install nodejs
RUN \
  cd /tmp && \
  wget https://github.com/joyent/node/archive/v0.12.0.tar.gz && \
  tar xvzf v0.12.0.tar.gz && \
  rm -f v0.12.0.tar.gz && \
  cd node-* && \
  ./configure && \
  CXX="g++ -Wno-unused-local-typedefs" make && \
  CXX="g++ -Wno-unused-local-typedefs" make install && \
  cd /tmp && \
  rm -rf /tmp/node-* 

# essential modules
RUN \
  npm install -g grunt-cli && \
  npm install forever -g
