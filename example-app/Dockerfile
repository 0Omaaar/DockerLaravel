FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
    libmcrypt-dev \
    libpq-dev \
    && docker-php-ext-install -j$(nproc) pdo_pgsql

COPY . /var/www

WORKDIR /var/www

RUN chown -R www-data:www-data /var/www

CMD ["php-fpm"]