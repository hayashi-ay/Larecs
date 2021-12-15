FROM nginx:1.20.2

COPY ./docker/develop/nginx/default.conf /etc/nginx/conf.d/default.conf
RUN mkdir /var/www/public

WORKDIR /var/www

EXPOSE 80
