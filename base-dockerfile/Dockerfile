# Use the official Ubuntu as the base image
FROM ubuntu:latest

# Set environment variables to non-interactive
ENV DEBIAN_FRONTEND=noninteractive

# Update the package repository and install necessary packages
RUN apt-get update && \
    apt-get install -y \
    curl \
    wget \
    gnupg \
    software-properties-common \
    openjdk-11-jdk \
    && apt-get clean

# Install Node.js 18
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - && \
    apt-get install -y nodejs

# Install Angular and Angular CLI
RUN npm install -g @angular/cli

# Install Cypress dependencies
RUN apt-get install -y \
    libgtk-3-0 \
    libnotify-dev \
    libgconf-2-4 \
    libgbm-dev \
    libxcb1 \
    xvfb

# Install Cypress
RUN npm install -g cypress

# Set the working directory
WORKDIR /app

# Start a shell session inside the container
CMD ["/bin/bash"]
