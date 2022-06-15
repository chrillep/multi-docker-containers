FROM php:8.1.7-fpm-alpine
RUN apk --no-cache add nginx supervisor nodejs npm yarn openssl git curl libc6-compat openssh zip
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/
RUN install-php-extensions opcache gd redis bcmath intl pcntl soap zip pdo_mysql
