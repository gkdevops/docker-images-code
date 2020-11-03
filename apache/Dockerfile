# This Dockerfile is to install, configure and deploy Apache Web Server

FROM ubuntu:12.04

MAINTAINER Goutham Kumar <chgoutam@gmail.com>

LABEL appName="offers" \
      version="3.8.9" \
      release="10-05-19"

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80

RUN apt-get update && apt-get install -y apache2 && apt-get clean

COPY index.html /var/www/

CMD ["/usr/sbin/apache2", "-D", "FOREGROUND"]
