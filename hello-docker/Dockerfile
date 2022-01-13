# Start with the base image
# Can either be an OS (FROM linux) or a specific setup (FROM node)
FROM node:alpine

# Copy our application files into a custom directory
# /app is a directory in the image, not a local one
COPY . /app

# Set the working directory to be the previously created /app
# Basically, all following instructions will be performed from the specified directory
WORKDIR /app

# Execute a command
CMD node app.js