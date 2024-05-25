# Using Ubuntu 22.04 as the base
FROM ubuntu:22.04

# Use /usr/src/app as our workdir
WORKDIR /usr/src/app

# Copy the script file
COPY script.sh .

# Update the repos
RUN apt update

# Install cURL
RUN apt install -y curl

# Executing the script!
CMD ./script.sh