FROM ubuntu:14.04

MAINTAINER Tom Rudick <tmrudick@gmail.com>

# Get wget so we can download the tarball
RUN apt-get update && \
    apt-get install -y wget && \
    apt-get clean

# Download and install the Go tarball
RUN wget http://golang.org/dl/go1.3.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go1.3.linux-amd64.tar.gz && \
    rm go1.3.linux-amd64.tar.gz

# Add the Go executables to our path
ENV PATH $PATH:/usr/local/go/bin

# Create a Go workspace directory
RUN mkdir /workspace
WORKDIR /workspace
ENV GOPATH /workspace

# To be used with a mounted volume in /workspace for development
