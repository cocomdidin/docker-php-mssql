FROM php:8.4-fpm

ENV ACCEPT_EULA=Y

# Retrieve official extension installer
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

# Install required PHP extensions; driver msodbcsql18 and dependencies handled automatically
RUN install-php-extensions \
    bcmath \
    ds \
    exif \
    gd \
    intl \
    opcache \
    pcntl \
    pdo_sqlsrv \
    redis \
    sqlsrv \
    zip

# Setting the work directory.
WORKDIR /var/www
