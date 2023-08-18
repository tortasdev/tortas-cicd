# Use the official Jenkins LTS image as the base image
FROM jenkins/jenkins:lts

# Set environment variables (if needed)
ENV JENKINS_HOME=/var/jenkins_home

# Switch to the root user to perform necessary operations
USER root

# Create the Jenkins home directory if it doesn't exist
RUN mkdir -p $JENKINS_HOME && chown -R jenkins:jenkins $JENKINS_HOME

# Switch back to the jenkins user
USER jenkins
