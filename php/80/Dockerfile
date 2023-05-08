FROM php:8.0.28-fpm

RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN docker-php-ext-enable mysqli pdo pdo_mysql

RUN apt-get update && apt-get install -y \
    libmagickwand-dev --no-install-recommends \
    && pecl install imagick \
	&& docker-php-ext-enable imagick

RUN apt-get install -y libzip-dev \
  && docker-php-ext-configure zip \
  && docker-php-ext-install zip \
  && docker-php-ext-enable zip

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd

RUN docker-php-ext-install bcmath

RUN docker-php-ext-install bz2

RUN docker-php-ext-install calendar

RUN docker-php-ext-install dba

RUN docker-php-ext-install exif

RUN docker-php-ext-install gettext

RUN apt-get install -y libgmp-dev
RUN docker-php-ext-install gmp