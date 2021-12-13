FROM php:8.0-fpm

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

COPY api/. /var/www/
COPY docker/develop/php/php.ini /user/local/etc/php/

RUN apt-get update -y \
  && apt-get install -y git

WORKDIR /var/www

EXPOSE 9000
