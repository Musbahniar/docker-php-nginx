FROM php:7.4-fpm
RUN apt-get update
RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev
RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN docker-php-ext-install bz2
RUN docker-php-ext-configure gd --with-freetype --with-jpeg 
RUN docker-php-ext-install -j$(nproc) gd
RUN apt-get install -y libmcrypt-dev
RUN docker-php-ext-install -j$(nproc) mcrypt

# RUN docker-php-ext-install intl (ketergantungan dgn composer)
# FROM php:7.4-fpm
# #install ext-gd
# RUN apt-get update && apt-get install -y \
# 		libfreetype6-dev \
# 		libjpeg62-turbo-dev \
# 		libpng-dev \
#   && docker-php-ext-install mysqli \
#   && docker-php-ext-install intl \
	# && docker-php-ext-configure gd --with-freetype --with-jpeg \
	# && docker-php-ext-install -j$(nproc) gd \
# RUN docker-php-ext install mysqli
    # bz2 \
    # intl \
#install ext-mcrypt
# RUN apt-get install -y \
#     libmcrypt-dev \
#     && docker-php-ext-install -j$(nproc) mcrypt
