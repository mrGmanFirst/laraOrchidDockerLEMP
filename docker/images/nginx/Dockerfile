FROM nginx:stable-alpine

RUN addgroup -g 1000 laravel && adduser -G laravel -g laravel -s /bin/sh -D laravel

RUN mkdir -p /var/www/orchid

RUN chown laravel:laravel /var/www/orchid

WORKDIR /var/www/orchid