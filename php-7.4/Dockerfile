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
        php7.4-cli \
        php7.4-fpm \
        php7.4-json \
        php7.4-intl \
        php7.4-curl \
        php7.4-mysql \
        php7.4-gd \
        php7.4-sqlite3 \
        php7.4-ldap \
        php7.4-opcache \
        php7.4-soap \
        php7.4-zip \
        php7.4-mbstring \
        php7.4-bcmath \
        php7.4-xmlrpc \
        php7.4-xsl \
        php7.4-bz2 \
        php7.4-gmp \
        php-apcu \
        php-redis \
        php-memcache \
        php-memcached

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin/ --filename=composer \
    && curl -LO https://deployer.org/deployer.phar \
    && mv deployer.phar /usr/local/bin/dep \
    && chmod +x /usr/local/bin/dep


