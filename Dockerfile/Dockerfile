FROM jenkins/jenkins:lts

# Switch to root user to install dependencies
USER root

# Fix package database corruption, update and install dependencies
RUN rm -rf /var/lib/dpkg/info && \
    apt-get clean && \
    apt-get update && \
    apt-get install -y --fix-missing make g++

# Switch back to jenkins user (good practice)
USER jenkins
