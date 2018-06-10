FROM php:7-apache

COPY ./000-default.conf /etc/apache2/sites-enabled/000-default.conf

RUN apt-get update -y && apt-get install -y libpng-dev curl libcurl4-openssl-dev

RUN docker-php-ext-install pdo pdo_mysql gd curl

RUN a2enmod rewrite
RUN service apache2 restart

ENV ALLOW_OVERRIDE true  