FROM namoshek/php-mssql:8.4-fpm-alpine

# Install build tools and dependencies for OpenSwoole
RUN apk add --no-cache --virtual .build-deps \
      alpine-sdk \
      autoconf \
      pcre2-dev \
      openssl-dev \
      curl-dev \
      zlib-dev \
      linux-headers \
    && pecl install openswoole \
    && docker-php-ext-enable openswoole \
    && apk del .build-deps