FROM php:7.2-fpm

ADD . /app

WORKDIR /app

RUN apt-get update

RUN apt-get install -y apt-utils

RUN apt-get install -y locales

RUN apt-get install -y nano

RUN apt-get install -y nginx

RUN echo "en_US.UTF-8 UTF-8" > /etc/locale.gen
RUN locale-gen

RUN rm -f /etc/nginx/nginx.conf
RUN rm -f /etc/nginx/conf.d/*
RUN cp -r /app/provisioning/nginx/* /etc/nginx

EXPOSE 80
