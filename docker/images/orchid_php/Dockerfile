FROM php:8.3.0-fpm-alpine

RUN addgroup -g 1000 laravel && adduser -G laravel -g laravel -s /bin/sh -D laravel

RUN mkdir -p /var/www/orchid

RUN chown laravel:laravel /var/www/orchid

WORKDIR /var/www/orchid

COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

RUN apk add nodejs npm

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions \
    mysqli \
    pdo_mysql \
    PDO_ODBC \
    redis \
    zip