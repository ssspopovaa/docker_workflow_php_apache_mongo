FROM httpd:2.4.33-alpine
RUN apk update; \
    apk upgrade;
# Copy apache vhost file to proxy php requests to php-fpm container
#COPY slr.apache.conf /usr/local/apache2/conf/slr.apache.conf

RUN sed -i '/LoadModule rewrite_module/s/^#//g' /usr/local/apache2/conf/httpd.conf

RUN echo "Include /usr/local/apache2/conf/slr.apache.conf" \
    >> /usr/local/apache2/conf/httpd.conf