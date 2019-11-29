FROM php:7.2-fpm
RUN echo "deb http://mirrors.ustc.edu.cn/debian stable main contrib non-free\ndeb-src http://mirrors.ustc.edu.cn/debian stable main contrib non-free\ndeb http://mirrors.ustc.edu.cn/debian stable-proposed-updates main contrib non-free\ndeb-src http://mirrors.ustc.edu.cn/debian stable-proposed-updates main contrib non-free">/etc/apt/sources.list
RUN apt -qy install $PHPIZE_DEPS \
	&& pecl install xdebug \
	&& docker-php-ext-install mysqli \
	&& docker-php-ext-enable xdebug
