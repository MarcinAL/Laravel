FROM php:8.2-fpm

RUN apt-get update && apt-get install -y \
    zip unzip curl libpng-dev libjpeg-dev libonig-dev libxml2-dev libzip-dev \
    libpq-dev libicu-dev libmcrypt-dev git \
    && docker-php-ext-install pdo_mysql mbstring zip exif pcntl bcmath gd intl sockets

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer


COPY php.ini /usr/local/etc/php/php.ini
