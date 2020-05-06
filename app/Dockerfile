FROM php:7.4-fpm
RUN apt-get update \
  && apt-get install -y libpq-dev libonig-dev \
  && docker-php-ext-install mbstring pdo pdo_pgsql

COPY --from=composer /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/html
