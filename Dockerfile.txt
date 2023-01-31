FROM ubuntu
MAINTAINERS aish
COPY . ./var/www/html/
RUN apt-get update -y && apt-get install nginx -y
EXPOSE 80
CMD [ "systemctl","start","nginx" ]
