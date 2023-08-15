# Use the official Jenkins LTS as the base image
FROM jenkins/jenkins:lts

# Switch to root user for installation
USER root

# Install necessary packages
RUN apt-get update && \
    apt-get install -y \
    openjdk-11-jdk \
    && apt-get clean

# Switch back to Jenkins user
USER jenkins

# Expose Jenkins port
EXPOSE 8080
