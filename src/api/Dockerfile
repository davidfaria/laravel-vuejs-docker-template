# build stage
FROM bitnami/php-fpm:7.4

WORKDIR /app

COPY php.ini /opt/bitnami/php/etc/conf.d/php.ini

COPY database/ /app/database/
COPY tests/ /app/tests/

COPY composer.json /app/
COPY composer.lock /app/

RUN composer install

COPY . /app

CMD php artisan serve --host=0.0.0.0 --port=8181

EXPOSE 8181


