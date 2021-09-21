FROM  ubuntu/apache2:2.4-20.04_edge
LABEL "Testing install Apache2:2.4"="via dockerfile"

###OPTIONAL
COPY ./index.html /var/www/html/index.html
###

RUN apt-get update && apt-get install -y iputils-ping net-tools curl nano


