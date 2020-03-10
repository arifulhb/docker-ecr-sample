FROM php:7.3-fpm-stretch

ARG NOVA_USER

RUN echo "'name \n ${NOVA_USER}'"
# Work Directory
WORKDIR /var/www/app

# Install packages
RUN apt-get update \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

CMD ["php-fpm"]

COPY ./docker/app/php/local.ini /usr/local/etc/php/conf.d/local.ini

COPY ./src /var/www/app

EXPOSE 9000
