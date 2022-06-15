#FROM node:lts-alpine AS node
#FROM nginx:1.21.6-alpine AS nginx
#FROM php:8.1.5-fpm-alpine as php

#FROM ghcr.io/yaytrade/nginx:latest
#WORKDIR /app

FROM ghcr.io/yaytrade/php:latest as base
WORKDIR /app
COPY --from=node:lts-alpine /usr/local/bin /usr/local/bin
COPY --from=node:lts-alpine /usr/local/lib /usr/local/lib
COPY --from=node:lts-alpine /opt /opt
COPY --from=nginx:1.21.6-alpine /usr/sbin/nginx /usr/sbin/nginx
COPY --from=nginx:1.21.6-alpine /usr/sbin/nginx-debug /usr/sbin/nginx-debug
COPY --from=nginx:1.21.6-alpine /usr/lib /usr/lib
