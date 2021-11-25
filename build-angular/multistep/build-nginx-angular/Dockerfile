##publish in docker hub, ryanrek007/nginx-debian-webserver:angular, using only for deploying nginx with app angular.js
FROM nginx:latest
LABEL "Install nginx "="customize version by Ryan"

WORKDIR /etc/nginx

RUN mkdir -p /var/www/html

RUN mv /usr/share/nginx/html/index.html /var/www/html/

COPY ./default.conf /etc/nginx/conf.d/

COPY ./nginx.conf /etc/nginx/

RUN apt-get update && apt-get install nano

ENV TZ=Asia/Jakarta

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone



