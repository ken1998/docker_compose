FROM ubuntu

MAINTAINER ken1998
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y apache2 \
	php7.2 \
	php7.2-fpm \
	php7.2-mysql \
	php7.2-mbstring \
	php7.2-zip \
	php7.2-xml \
	php7.2-pdo

EXPOSE 80

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

ADD ./apache2.conf /etc/apache2/apache2.conf
ADD ./content/ /var/www/html/

ENTRYPOINT ["/usr/sbin/apachectl","-DFOREGROUND"]
