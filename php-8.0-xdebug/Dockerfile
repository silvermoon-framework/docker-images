FROM silvermoonframework/php-8.0:latest

COPY xdebug.ini /etc/php/8.0/mods-available/xdebug.ini

RUN apt-get install -y php8.0-dev \
    && pecl install xdebug-3.0.1 \
    && ln -s /etc/php/8.0/mods-available/xdebug.ini /etc/php/8.0/cli/conf.d/20-xdebug.ini
