FROM nginx:latest
LABEL "Testing install nginx"="customize version by Ryan"
#optional
COPY ./info.php /usr/share/nginx/html/index.html
#

RUN apt-get update && apt-get install -y iputils-ping net-tools vim wget

RUN apt -y install lsb-release apt-transport-https ca-certificates

RUN wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg

RUN echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | tee /etc/apt/sources.list.d/ph>

RUN apt-get update

RUN apt -y install php7.4-fpm
