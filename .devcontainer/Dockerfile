FROM node:latest

# Install IG publisher dependencies
RUN apt-get update && \
    apt-get install -y \
        jekyll \
        graphviz \
        wget

# Download and install latest JDK 23 (using .deb package)
RUN wget -O jdk.deb "https://download.oracle.com/java/23/latest/jdk-23_linux-x64_bin.deb" && \
    apt-get update && \
    apt-get install -y ./jdk.deb && \
    rm jdk.deb && rm -rf /var/lib/apt/lists/*

# Set working directory (important for volume mounting)
WORKDIR /app