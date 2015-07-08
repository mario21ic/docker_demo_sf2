FROM php:5.6-apache
MAINTAINER Mario Inga <mario21ic@gmail.com>

RUN apt-get update
RUN apt-get install -y php5-curl php5-mysql php5-pgsql php5-memcache php5-memcached \
    php5-mongo php5-redis

RUN ln -s /etc/apache2/mods-available/rewrite.load /etc/apache2/mods-enabled
COPY ./php.ini /usr/local/etc/php/
COPY ./default.conf /etc/apache2/sites-enabled/
#RUN sed -i 's/AllowOverride None/AllowOverride All/g' -l 11 /etc/apache2/sites-available/default
