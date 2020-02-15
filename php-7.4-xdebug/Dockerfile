FROM silvermoonframework/php-7.4:latest

COPY xdebug.ini /etc/php/7.4/mods-available/xdebug.ini

RUN apt-get install -y php7.4-dev \
    && pecl install xdebug-2.9.1 \
    && ln -s /etc/php/7.4/mods-available/xdebug.ini /etc/php/7.4/cli/conf.d/20-xdebug.ini
