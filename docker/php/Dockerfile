FROM php:7.4-fpm

# Install PHP extensions
RUN apt-get update && apt-get install -y \
    libzip-dev \
    unzip \
    && docker-php-ext-install zip \
    && docker-php-ext-install pdo pdo_mysql

# Install Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/symfony

# Copy composer.json and composer.lock (if it exists) to the container
COPY ../../composer.json ./

# Install Symfony libraries
RUN composer install

EXPOSE 9000
