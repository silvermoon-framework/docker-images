FROM debian:10.1-slim

RUN apt-get update \
   && apt-get install -y git curl wget python build-essential vim parallel rsync unzip zip \
   && apt-get install -y apt-transport-https lsb-release ca-certificates \
   && wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg \
   && echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | tee /etc/apt/sources.list.d/php.list \
   && apt-get update

# Install php environment
RUN apt-get install -y \
        graphicsmagick \
        ghostscript \
        php8.0-cli \
        php8.0-fpm \
        php8.0-intl \
        php8.0-curl \
        php8.0-mysql \
        php8.0-gd \
        php8.0-sqlite3 \
        php8.0-ldap \
        php8.0-opcache \
        php8.0-soap \
        php8.0-zip \
        php8.0-mbstring \
        php8.0-bcmath \
        php8.0-xsl \
        php8.0-bz2 \
        php8.0-gmp \
        php-apcu \
        php-redis \
        php-memcache \
        php-memcached

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin/ --filename=composer \
    && curl -LO https://deployer.org/deployer.phar \
    && mv deployer.phar /usr/local/bin/dep \
    && chmod +x /usr/local/bin/dep
