FROM nginx:latest
LABEL "Testing install nginx"="customize version by Ryan"
#optional
COPY ./info.php /usr/share/nginx/html/index.html
#
RUN apt-get update && apt-get install -y iputils-ping net-tools curl nano
