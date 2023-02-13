FROM php:7.4-apache

RUN apt-get update
RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN a2enmod rewrite
RUN docker-php-ext-enable mysqli
RUN apt-get install -y libpq-dev
RUN apt-get install -y zlib1g-dev libzip-dev libpng-dev libwebp-dev
RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libgd-dev
RUN docker-php-ext-configure gd --with-jpeg=/usr/include/ --with-freetype=/usr/include/ --with-webp=/usr/include/
RUN docker-php-ext-install gd
RUN docker-php-ext-install zip
RUN service apache2 restart