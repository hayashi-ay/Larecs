FROM nginx:1.20.2

COPY api/public/. /var/www/public
COPY ./docker/develop/nginx/default.conf /etc/nginx/conf.d/default.conf

WORKDIR /var/www

EXPOSE 80
