FROM php:7.2-apache

ENV DEBIAN_FRONTEND noninteractive

ADD default.conf /etc/apache2/sites-available/000-default.conf
ADD php.ini /usr/local/etc/php/php.ini

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP root
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_PID_FILE /var/run/apache2.pid
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2

RUN mkdir -p $APACHE_RUN_DIR $APACHE_LOCK_DIR $APACHE_LOG_DIR
RUN a2enmod rewrite