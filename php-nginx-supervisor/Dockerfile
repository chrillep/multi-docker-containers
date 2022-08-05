FROM php:8.1.9-fpm-alpine
RUN apk --no-cache add openssl nginx supervisor
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/
RUN install-php-extensions opcache gd redis bcmath intl pcntl soap zip pdo_mysql
