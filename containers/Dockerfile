FROM php:7.3-fpm
RUN apt-get update && apt-get install -y git
RUN docker-php-ext-install mysqli
WORKDIR /var/www/html
RUN git init  
ADD config .git
RUN git pull
RUN chown -R www-data. .
RUN mv wp-config-sample.php wp-config.php

