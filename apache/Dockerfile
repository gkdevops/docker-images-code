# This Dockerfile is to install, configure and deploy Apache Web Server

FROM ubuntu:20.04

LABEL email=chgoutam@gmail.com

WORKDIR /var/www/html

ENV DEBIAN_FRONTEND=noninteractive

LABEL appName="offers" version="3.8.9" release="10-05-19" team_name="devops team"

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80
EXPOSE 443

RUN apt-get update && apt-get install -y apache2 apache2-utils --no-install-recommends && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY Dockerfile .

COPY source-code/index.html .

CMD ["apache2ctl", "-D", "FOREGROUND"]
