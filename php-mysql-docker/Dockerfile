FROM php:8.0-apache
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
RUN docker-php-ext-install pdo && docker-php-ext-enable pdo
RUN docker-php-ext-install pdo_mysql && docker-php-ext-enable pdo_mysql
RUN a2enmod rewrite

# setting timezone to europe
RUN echo "date.timezone = \"Europe/Berlin\" " >> /usr/local/etc/php/php.ini
RUN cp /usr/share/zoneinfo/Europe/Rome /etc/localtime && echo "Europe/Berlin" > /etc/timezone
