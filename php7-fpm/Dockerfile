FROM php:7-fpm
ARG TIMEZONE

RUN apt-get update && apt-get install -y openssl git unzip

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Set timezone
RUN ln -snf /usr/share/zoneinfo/${TIMEZONE} /etc/localtime && echo ${TIMEZONE} > /etc/timezone
RUN printf '[PHP]\ndate.timezone = "%s"\n', ${TIMEZONE} > /usr/local/etc/php/conf.d/tzone.ini
RUN "date"

RUN apt-get update && apt-get install -y libmcrypt-dev mariadb-client \
    && docker-php-ext-install pdo_mysql

RUN apt-get update && apt-get install -y procps

RUN usermod -u 1000 www-data

WORKDIR /var/www/app
RUN chown -R www-data:www-data /var/www/app
USER www-data

#RUN git clone https://github.com/laravel/laravel.git .

#RUN composer install
