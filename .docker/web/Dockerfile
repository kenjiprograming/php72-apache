FROM php:7.2-apache

# Install required packages
RUN apt-get update && apt-get install -y \
  curl libxml2 libxml2-dev zlib1g-dev libzip-dev git vim zip unzip

# Install PHP extensions
RUN docker-php-ext-install zip pdo_mysql

# Enable Apache mod_rewrite
RUN a2enmod rewrite

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php --install-dir=/usr/local/bin --filename=composer

# Copy custom PHP configuration
COPY ./php.ini /usr/local/etc/php/

# Copy custom Apache site configuration
COPY 000-default.conf /etc/apache2/sites-available/

# Ensure the right file permissions
RUN chown -R www-data:www-data /var/www/html