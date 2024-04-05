FROM wordpress:latest
WORKDIR /var/www/html/

COPY ./.env .

RUN pecl install xdebug && docker-php-ext-enable xdebug;
COPY ./configs/xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

RUN curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar && \
    chmod +x wp-cli.phar && \
    mv wp-cli.phar /usr/local/bin/wp