FROM ubuntu
RUN apt-get update \
    && apt-get install nginx -y \
    && echo "daemon off;" >> /etc/nginx/nginx.conf
ADD default /etc/nginx/sites-available/
EXPOSE 80
CMD echo "$HOSTNAME" > index.html && cp index.html /usr/share/nginx/html/index.html && service nginx start
