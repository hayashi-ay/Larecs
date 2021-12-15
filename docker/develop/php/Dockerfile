FROM php:8.0-fpm

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

COPY api/. /var/www/
COPY docker/develop/php/php.ini /user/local/etc/php/

WORKDIR /var/www

RUN apt-get update -y \
  && apt-get install -y git

RUN composer install

RUN chown -R www-data:www-data storage

EXPOSE 8999
