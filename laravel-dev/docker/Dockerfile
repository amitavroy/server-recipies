FROM php:8.1.1-apache-buster

RUN apt-get update -yqq && \
    apt-get update --fix-missing && \
    apt-get install -y apt-utils zip unzip curl && \
    apt-get install -y nano && \
    apt-get install -y libzip-dev libpq-dev libmcrypt-dev

RUN docker-php-ext-install mysqli && \
    docker-php-ext-install pdo_mysql && \
    docker-php-ext-install bcmath

RUN rm -rf /var/lib/apt/lists/*

RUN php -r "readfile('http://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer

COPY default.conf /etc/apache2/sites-enabled/000-default.conf

WORKDIR /var/www/app

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]

EXPOSE 80
