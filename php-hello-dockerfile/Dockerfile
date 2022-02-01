FROM php:7.0-apache
RUN sed -i "s/Listen 80/Listen 8080/g" /etc/apache2/ports.conf && \
sed -i "s/#ServerName www.example.com/ServerName 0.0.0.0:8080/g" /etc/apache2/sites-enabled/000-default.conf && \
sed -i "s/<VirtualHost *:80>/<VirtualHost *:8080>/g" /etc/apache2/sites-enabled/000-default.conf && \
chgrp -R 0 /var/www/html && chmod -R g=u /var/www/html
COPY src/ /var/www/html
USER 1001
EXPOSE 8080
