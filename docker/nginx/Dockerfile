FROM nginx:latest

CMD ["nginx"]

# Work Directory
WORKDIR /var/www/app

COPY ./nginx.conf /etc/nginx/nginx.conf
COPY ./conf.d /etc/nginx/conf.d
COPY ./sites/default.conf /etc/nginx/sites-available/default.conf

EXPOSE 80 443
