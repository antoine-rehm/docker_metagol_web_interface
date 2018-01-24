FROM php:fpm
RUN apt update && apt install -y yap
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli