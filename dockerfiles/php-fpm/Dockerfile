FROM php:8.2-fpm

RUN apt-get update && apt-get install -y procps

COPY --from=composer /usr/bin/composer /usr/bin/composer

COPY ./config/php-fpm.conf /usr/local/etc/php-fpm.conf
COPY ./config/php.ini /usr/local/etc/php/php.ini

RUN docker-php-ext-install mysqli