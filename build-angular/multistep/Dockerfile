##STAGE FOR BUILDING NODE AND ANGULAR ==> FOR BUILDER NODE
FROM ryanrek007/angular:latest as build-stage
LABEL "Install node.js and angular"="customize version by Ryan"

##installing node and dependency
WORKDIR /app
COPY package*.json ./
RUN npm install

##aftering installing dependency, copy application/your code
COPY . .

ARG configuration=production

RUN npm run build -- --output-path=./dist --configuration $configuration

##========================================================================================
##STAGE FOR PUBLISH APP NODE AND ANGULAR WITH NGINX ==> PUBLISH IMAGE DOCKER FOR PRODUCTION
FROM ryanrek007/nginx-debian-webserver:angular

COPY --from=build-stage /app/dist /var/www/html
