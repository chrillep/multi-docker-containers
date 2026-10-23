FROM php:8.5.12-fpm-alpine@sha256:f09d9172dd28b8696aef729ca2c2081a132c1f8d581218c99497d552c82a92df
RUN apk --no-cache add openssl nginx supervisor
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
