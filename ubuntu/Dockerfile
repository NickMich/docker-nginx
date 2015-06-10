FROM ubuntu:14.04
MAINTAINER nickmich

RUN apt-get update
RUN apt-get -y upgrade
RUN apt-get -y install nginx
RUN echo "nginx -c /opt/nginx/nginx.conf && tail -f /var/log/nginx/access.log" > /start.sh

EXPOSE 8777
VOLUME /opt/nginx/
VOLUME /var/nginx/

ENTRYPOINT ["bash", "/start.sh"]
