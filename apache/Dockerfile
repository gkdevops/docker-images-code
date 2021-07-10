# This Dockerfile is to install, configure and deploy Apache Web Server

FROM ubuntu:20.04

# MAINTAINER Goutham Kumar <chgoutam@gmail.com>

ENV DEBIAN_FRONTEND=noninteractive

LABEL appName="offers" \
      version="3.8.9" \
      release="10-05-19" \
      team_name="devops team"

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80
EXPOSE 443

RUN apt-get update && apt-get install -y apache2 apache2-utils && apt-get clean

COPY index.html /var/www/html/

CMD ["apache2ctl", "-D", "FOREGROUND"]
