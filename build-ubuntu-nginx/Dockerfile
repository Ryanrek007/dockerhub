FROM nginx:latest
LABEL "Install nginx server and php7.4-fpm"="customize version by Ryan"

COPY ./info.html /usr/share/nginx/html/index.html

RUN mkdir /var/www

RUN mkdir /var/www/html

RUN cp /usr/share/nginx/html/index.html /var/www/html/

COPY ./nginx/default.conf /etc/nginx/conf.d/

COPY ./nginx1-bak.conf /etc/nginx/

RUN apt-get update && apt-get install -y iputils-ping net-tools nano wget

RUN apt -y install lsb-release apt-transport-https ca-certificates

RUN wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg

RUN echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | tee /etc/apt/sources.list.d/php.list

RUN apt-get update

RUN apt -y install php7.4-fpm

ENV TZ=Asia/Jakarta

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
