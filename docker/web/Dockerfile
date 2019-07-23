FROM php:7.3.6-apache
MAINTAINER Walderlan Sena <walderlan@mybread.biz>
LABEL docker-php-mongo.version="1.0.0"
RUN a2enmod rewrite
RUN service apache2 restart
RUN apt update && apt install -y git
RUN apt-get install -y zlib1g-dev
RUN apt-get install -y libzip-dev unzip
RUN docker-php-ext-install zip
RUN pecl install mongodb
RUN echo "extension=mongodb.so" >> /usr/local/etc/php/conf.d/mongodb.ini
