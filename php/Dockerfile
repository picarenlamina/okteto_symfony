# Dockerfile para instalar extensiones de mysqli y pdo
FROM php:8.0-apache
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
RUN docker-php-ext-install pdo pdo_mysql
RUN apt-get update && apt-get upgrade -y

#https://accesto.com/blog/simple-docker-setup-for-symfony-project/
RUN a2enmod rewrite
#RUN wget https://getcomposer.org/download/2.0.9/composer.phar  
RUN wget -O composer-setup.php https://getcomposer.org/installer
RUN mv composer.phar /usr/bin/composer 
RUN chmod +x /usr/bin/composer
#COPY apache.conf /etc/apache2/sites-enabled/000-default.conf

