FROM php:8.2.7-fpm-alpine
RUN apk --no-cache add nginx supervisor nodejs npm yarn openssl git curl libc6-compat openssh zip
COPY --from=wordpress:cli /usr/local/bin/wp /usr/local/bin/wp
ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/
RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions \
    @composer \
    bcmath \
    exif \
    gd \
    intl \
    gettext \
    mysqli \
    opcache \
    pcntl \
    pdo_mysql \
    pdo_pgsql \
    redis \
    soap \
    swoole \
    zip