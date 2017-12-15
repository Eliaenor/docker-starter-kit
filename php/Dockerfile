# Use an official PHP as a parent image
FROM php:7.2.0-fpm

# Set the working directory to /app
WORKDIR /php

# Copy the current directory contents into the container at /app
ADD ../ /php

# Install Composer
RUN apt-get update && \
    apt-get install -y --no-install-recommends git zip

RUN curl --silent --show-error https://getcomposer.org/installer | php

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME PHP

# Run app.py when the container launches
CMD [ "php", "-r", "echo('Hello World !!\n');" ]
