#
# Ubuntu Dockerfile, use source image in China
#
# https://github.com/joecliff/docker-ubuntu
#

# Pull base image.
FROM ubuntu:14.04

# Change source list
RUN mv /etc/apt/sources.list /etc/apt/sources.list.bk
ADD ./sources.list /etc/apt/
RUN apt-get update && apt-get -y upgrade 

# Base lib
RUN \
  apt-get install -y g++ make unzip wget vim && \
  apt-get install -y python git

# Add files.
ADD root/.bashrc /root/.bashrc
ADD root/.gitconfig /root/.gitconfig
ADD root/scripts /root/scripts

# Set environment variables.
ENV HOME /root

# Define working directory.
WORKDIR /root

# Define default command.
CMD ["bash"]
