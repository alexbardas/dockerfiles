# Pull base image
FROM ubuntu:14.04

# Make bash the default shell
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

# Install
RUN apt-get update
RUN apt-get -y upgrade 
RUN apt-get install -y curl wget sed git vim htop silversearcher-ag

# Add dotfiles
RUN mkdir -p ~/dotfiles && git clone https://github.com/alexbardas/dotfiles.git ~/dotfiles && \
  rm -rf ~/dotfiles/.git && \ 
  ls -ad ~/dotfiles/{.,}* | tail -n +3 | xargs -I {} cp -p {} ~/ && \
  ~/bootstrap.sh && \
  rm -rf ~/dotfiles ~/bootstrap.sh

# Working directory
ENV HOME /root

# Default command
CMD ["bash"]

