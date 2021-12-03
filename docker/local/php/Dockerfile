FROM php:8.0-fpm

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN apt-get update -y \
  && apt-get install -y git

WORKDIR /var/www

ENV COMPOSER_ALLOW_SUPERUSER 1

RUN composer global require "laravel/installer"
