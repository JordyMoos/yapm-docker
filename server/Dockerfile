FROM php:7.1.7-fpm

RUN apt-get update \
  && apt-get install -y \
    curl \
    git \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /opt

RUN curl -sS https://getcomposer.org/installer | php -- --install- dir=/opt --filename=composer

RUN git clone https://github.com/marcusklaas/yapm-server.git /opt/server

WORKDIR /opt/server

ADD ./config.yml /opt/server/config.yml

RUN php /opt/composer install

