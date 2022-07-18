FROM php:7.1-fpm

RUN apt-get update && \
    apt-get install -y \
        zlib1g-dev \
        libcurl4-openssl-dev \
        pkg-config \
        libssl-dev \
        git\
        libmagickwand-dev \
        libpng-dev \
        libzip-dev \
        vim \
        nodejs \
        npm
RUN docker-php-ext-install \
    zip \
    pdo \
    pdo_mysql \
    gd \
    bcmath
RUN pecl install yaf-3.0.5 \
    && docker-php-ext-enable yaf
RUN pecl install mongodb-1.7.5 \
    && docker-php-ext-enable mongodb

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
