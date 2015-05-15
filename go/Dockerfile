FROM alexbardas/ubuntu

# Install Go
RUN mkdir -p /golang 
RUN curl https://storage.googleapis.com/golang/go1.4.2.linux-amd64.tar.gz | tar xvzf - -C /golang --strip-components=1

# Set environment variables.
ENV GOROOT /golang
ENV GOPATH $HOME/go
ENV PATH $GOROOT/bin:$GOPATH/bin:$PATH

# Define working directory.
WORKDIR $HOME/go

# Define default command.
CMD ["bash"]
 
