FROM php:7.1-apache
RUN apt-get update \
    && apt-get install -y \
        libfreetype6-dev libjpeg62-turbo-dev libpng-dev libmcrypt-dev zlib1g-dev \
        git vim unzip \
    && docker-php-ext-install pdo_mysql mysqli mbstring gd iconv mcrypt \
    && apt-get clean \
    && a2enmod headers \
    && a2enmod include \
    && a2enmod rewrite

# Apache config
COPY ./conf/00_virtualhost.conf /etc/apache2/sites-available/
RUN a2dissite '*default*' \
    && a2ensite 00_virtualhost \
    && service apache2 restart

# PHP config
COPY ./conf/php.ini /usr/local/etc/php/

# install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filen
