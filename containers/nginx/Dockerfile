FROM zaioll/nginx:latest

LABEL mainteiner 'Láyro Chrystofer <zaioll@protonmail.com>'

#RUN sed -i -E -e 's|worker_processes auto;|worker_processes 4;|g' /etc/nginx/nginx.conf
COPY php-fpm.conf /etc/nginx/conf.d/
COPY default.conf /etc/nginx/sites-enabled/default

EXPOSE 80 443
STOPSIGNAL SIGTERM
CMD nginx -g "daemon off;"