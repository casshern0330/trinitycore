FROM php:7.4-fpm
RUN sed -i "s@deb.debian.org@mirrors.tuna.tsinghua.edu.cn@g" /etc/apt/sources.list \
	&& apt-get update \
	&& apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev libgmp-dev libxml2-dev libonig-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd pdo pdo_mysql mbstring gmp soap
