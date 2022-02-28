FROM alpine:latest
RUN apk update
RUN apk add nginx
RUN adduser -D -g 'www' www
RUN mkdir /www
RUN chown -R www:www /var/lib/nginx
RUN chown -R www:www /www
RUN rm -v /etc/nginx/nginx.conf
ADD nginx.conf /etc/nginx/
COPY /www/index.html /usr/share/nginx/html/
ADD www /var/www/html/
EXPOSE 80
CMD /usr/sbin/nginx -g 'daemon off;'

