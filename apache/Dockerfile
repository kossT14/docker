#########################
# Apache installation
#########################

# Set the base image for this installation
FROM ubuntu:latest

# File author/ maintainer
MAINTAINER Constantin Voinea <cos.voinea@gmail.com>

# Install Apache
RUN apt-get update && apt-get -y upgrade && apt-get -y install\
    apache2

# Environment variables
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2
ENV APACHE_PID_FILE /var/run/apache2.pid

# Expose Apache
EXPOSE 80

# Copy repo into place
ADD ./ /var/www

# Start up Apache in the foreground, by default
CMD /usr/sbin/apache2ctl -D FOREGROUND
