FROM php:7.4-fpm

# Install necessary PHP extensions
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
# Optionally copy composer.lock if it exists
# COPY composer.lock ./

# Install Symfony and other PHP libraries
RUN composer install

EXPOSE 9000
