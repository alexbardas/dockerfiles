FROM alexbardas/ubuntu

RUN apt-get update && \
    apt-get install -y curl

# Install nodejs.
RUN curl -sL https://deb.nodesource.com/setup_0.12 | bash -
RUN apt-get install -y nodejs

# Define working directory.
WORKDIR $HOME/node

# Define default command.
CMD ["bash"]
