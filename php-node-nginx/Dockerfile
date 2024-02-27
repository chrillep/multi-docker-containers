FROM php:8.3.3-fpm-alpine@sha256:5642a2fd6c6121ea0aacc08db7ee211825b83a0fb8a47dd0c2682dacfa171639
RUN apk --no-cache add openssl nginx node
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