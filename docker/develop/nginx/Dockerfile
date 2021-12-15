FROM nginx:1.20.2

COPY api/. /var/www/
COPY ./docker/develop/nginx/default.conf /etc/nginx/conf.d/default.conf

RUN mkdir /run/php-fpm

WORKDIR /var/www

EXPOSE 80
