FROM php:8.3-fpm-bookworm

ENV COMPOSER_ROOT_VERSION=2.7.7

COPY --from=composer:2.7.7 /usr/bin/composer /usr/bin/composer
RUN apt update && apt install -y git zip unzip

USER www-data
WORKDIR /app

CMD ["composer", "start"]