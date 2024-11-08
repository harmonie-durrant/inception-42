FROM debian:buster

RUN		apt-get update
RUN		apt-get install -y nginx \
                openssl

RUN mkdir -p /etc/nginx/ssl
RUN openssl req -newkey rsa:4096 -x509 -sha256 -days 365 -nodes \
       -out /etc/nginx/ssl/rbryento.crt \
       -keyout /etc/nginx/ssl/rbryento.key \
       -subj "/C=FR/ST=Paris/L=Paris/O=42 School/OU=rbryento/CN=rbryento/"

COPY ./conf/nginx.conf /etc/nginx/conf.d

RUN mkdir -p /run/nginx

RUN chmod 755 /var/www/html
RUN chown -R www-data:www-data /var/www/html

EXPOSE	443

CMD ["nginx", "-g", "daemon off;"]