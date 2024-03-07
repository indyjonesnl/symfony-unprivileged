FROM php:8.3-fpm-alpine

RUN --mount=type=bind,from=mlocati/php-extension-installer:latest,source=/usr/bin/install-php-extensions,target=/usr/local/bin/install-php-extensions \
      install-php-extensions opcache

RUN mkdir /sock \
    && chown -R nobody:nobody /sock

VOLUME ["/sock"]

USER nobody
