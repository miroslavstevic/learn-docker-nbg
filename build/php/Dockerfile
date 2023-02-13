FROM php:7.4-apache

RUN apt-get update && \
    docker-php-ext-install mysqli pdo pdo_mysql && \
    a2enmod rewrite && \
    docker-php-ext-enable mysqli && \
    service apache2 restart
