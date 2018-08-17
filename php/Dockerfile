# see https://github.com/cmaessen/docker-php-sendmail for more information

FROM php:fpm

RUN apt-get update && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install mysqli pdo_mysql