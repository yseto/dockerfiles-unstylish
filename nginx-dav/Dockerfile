FROM nginx:1.11-alpine

VOLUME /dav
EXPOSE 80

COPY dav.conf /etc/nginx/conf.d/

CMD nginx -g 'daemon off;'
