FROM php:7.1.3-fpm
RUN mkdir /code \
   && mkdir /log \
   && mkdir /storage \
   && mkdir /storage/framework \
   && mkdir /storage/framework/cache \
   && mkdir /storage/framework/cache/data \
   && mkdir /storage/framework/sessions \
   && mkdir /storage/framework/views \
   && chown -R www-data:www-data /storage \
   && docker-php-ext-install pdo pdo_mysql \
   && rm -f /usr/local/etc/php-fpm.conf \
   && rm -f /usr/local/etc/php-fpm.d/docker.conf
COPY ./conf/php.ini /usr/local/etc/php/
COPY ./conf/php-fpm.conf /usr/local/etc/
COPY ./conf/php-fpm.d/docker.conf /usr/local/etc/php-fpm.d/
WORKDIR /code
VOLUME ["/code", "/log"]
