#########################
# PHP installation
#########################

# Set the base image for this installation
FROM my_apache

# File author/ maintainer
MAINTAINER Constantin Voinea <cos.voinea@gmail.com>

# Environment variables
# ENV PHPIZE_DEPS \
                autoconf \
                file \
                g++ \
                gcc \
                libc-dev \
                make \
                pkg-config \
                re2c

# Install PHP
RUN apt-get update && apt-get -y upgrade && apt-get -y install \
                $PHPIZE_DEPS \
                ca-certificates \
                curl \
                libedit2 \
                libsqlite3-0 \
                libxml2 \
                libjpeg-dev \
		            libpng-dev \
                xz-utils

# ENV PHP_INI_DIR /usr/local/etc/php
# RUN mkdir -p $PHP_INI_DIR/conf.d

# Expose php
EXPOSE 80

# Copy repo into place
ADD root /
ADD src /var/www
