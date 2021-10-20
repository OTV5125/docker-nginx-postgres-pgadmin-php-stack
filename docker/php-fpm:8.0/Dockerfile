FROM php:fpm-buster
RUN pecl install xdebug-3.1.1 && docker-php-ext-enable xdebug

RUN useradd -ms /bin/bash otv5125

COPY conf/www.conf /usr/local/etc/php-fpm.d/
RUN rm /usr/local/etc/php-fpm.d/zz-docker.conf
USER otv5125
CMD ["php-fpm", "--nodaemonize"]